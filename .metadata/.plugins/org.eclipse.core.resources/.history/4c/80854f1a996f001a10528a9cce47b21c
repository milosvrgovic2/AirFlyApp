package model;

import java.io.Serializable;
import javax.persistence.*;


/**
 * The persistent class for the aircraft database table.
 * 
 */
@Entity
@NamedQuery(name="Aircraft.findAll", query="SELECT a FROM Aircraft a")
public class Aircraft implements Serializable {
	private static final long serialVersionUID = 1L;

	@Id
	@GeneratedValue(strategy=GenerationType.IDENTITY)
	private int id;

	@Lob
	private byte[] slika;

	private String tip;

	//bi-directional many-to-one association to Company
	@ManyToOne
	@JoinColumn(name="prevoznik_id")
	private Company company;

	public Aircraft() {
	}

	public int getId() {
		return this.id;
	}

	public void setId(int id) {
		this.id = id;
	}

	public byte[] getSlika() {
		return this.slika;
	}

	public void setSlika(byte[] slika) {
		this.slika = slika;
	}

	public String getTip() {
		return this.tip;
	}

	public void setTip(String tip) {
		this.tip = tip;
	}

	public Company getCompany() {
		return this.company;
	}

	public void setCompany(Company company) {
		this.company = company;
	}

}