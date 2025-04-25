AWS VPC con Terraform
Este repositorio contiene una implementación de infraestructura como código (IaC) utilizando Terraform para desplegar una red virtual (VPC) en AWS. Incluye la creación de subredes públicas y privadas, instancias EC2, tablas de rutas, un Internet Gateway y un VPC Endpoint.

Características
Creación de una VPC personalizada.

Subred pública con su rango de IPs.

Subred privada con su rango de IPs.

Internet Gateway para acceso a Internet desde la subred pública.

Instancia EC2 en la subred pública.

Instancia EC2 en la subred privada.

Tablas de rutas asociadas a cada subred.

Configuración de un VPC Endpoint para servicios privados de AWS.

Estructura del Proyecto
main.tf: Define los recursos principales de la infraestructura.

variables.tf: Contiene las variables utilizadas en el proyecto.

outputs.tf: Especifica las salidas que proporciona Terraform después de la implementación.

provider.tf: Configura el proveedor de AWS para Terraform.

remote_backend_s3.tf: Configura el backend remoto en S3 para el estado de Terraform.

terraform.tfvars: Define los valores específicos para las variables.

Directorios adicionales:

networking/: Configuración de la red (VPC, subredes, etc.).

ec2/: Definición de las instancias EC2.

security-groups/: Configuración de los grupos de seguridad.

vpc-endpoint/: Configuración del VPC Endpoint.

Prerrequisitos
Tener una cuenta de AWS con las credenciales configuradas.

Instalar Terraform (versión 1.0 o superior).

Configurar el archivo terraform.tfvars con los valores adecuados para tu entorno.

Uso
Clona este repositorio:
git clone https://github.com/richardaguirre1/aws-terraform-vpc.git
cd aws-terraform-vpc

