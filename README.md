# CKAD-Prep

This repository contains a collection of real-world scenarios to help you prepare for the Certified Kubernetes Application Developer (CKAD) exam. Each scenario is designed to test your understanding of specific Kubernetes concepts and your ability to apply them in practical situations.

## Scenarios

Below is a list of available scenarios. Click on a scenario name to navigate to its detailed description and instructions.

- [Custom Flask Application Image](./scenarios/custom-image-flask-app/README.md)

## How to Use This Repository

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd CKAD-Prep
   ```
2. **Navigate to a scenario:**
   Each scenario is contained within its own directory under the `scenarios` folder.
   ```bash
   cd scenarios/<scenario-name>
   ```
3. **Follow the instructions:**
   Read the `README.md` file within the scenario's directory. It will outline the objective, steps to complete, and expected outcomes.
4. **Practice!**
   Work through the scenario, applying your Kubernetes knowledge.

## Contributing

Contributions are welcome! If you have a new scenario idea or improvements to existing ones, please follow these steps:

1. **Fork the repository.**
2. **Create a new branch** for your scenario or changes.
3. **Add your scenario** or make your modifications. Ensure you include a detailed `README.md` for any new scenarios, following the existing format.
4. **Test your changes** thoroughly.
5. **Submit a pull request** for review.

## Prerequisites

To work through these scenarios, you will generally need the following installed:

- **Docker:** For building and running container images. Refer to the [official Docker documentation](https://docs.docker.com/get-docker/) for installation instructions.
- **kubectl:** The Kubernetes command-line tool. Refer to the [official Kubernetes documentation](https://kubernetes.io/docs/tasks/tools/install-kubectl/) for installation.
- **A Kubernetes cluster:** This could be Minikube, Kind, Docker Desktop's Kubernetes, or a cloud-based Kubernetes service. Each scenario might have specific version recommendations if applicable.

Happy learning, and good luck with your CKAD exam!
