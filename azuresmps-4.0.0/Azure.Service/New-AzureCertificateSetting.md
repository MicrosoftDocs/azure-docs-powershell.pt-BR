---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945932"
---
# <span data-ttu-id="23001-101">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="23001-101">New-AzureCertificateSetting</span></span>

## <span data-ttu-id="23001-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23001-102">SYNOPSIS</span></span>
<span data-ttu-id="23001-103">Cria um objeto de configuração de certificado para um certificado em um serviço.</span><span class="sxs-lookup"><span data-stu-id="23001-103">Creates a certificate setting object for a certificate is in a service.</span></span>

## <span data-ttu-id="23001-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23001-104">SYNTAX</span></span>

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="23001-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23001-105">DESCRIPTION</span></span>
<span data-ttu-id="23001-106">O cmdlet **New-AzureCertificateSetting** cria um objeto de configuração de certificado para um certificado que está em um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="23001-106">The **New-AzureCertificateSetting** cmdlet creates a certificate setting object for a certificate that is in an Azure service.</span></span>

<span data-ttu-id="23001-107">Você pode usar um objeto de configuração de certificado para criar um objeto de configuração usando o cmdlet **Add-AzureProvisioningConfig** .</span><span class="sxs-lookup"><span data-stu-id="23001-107">You can use a certificate setting object to create a configuration object by using the **Add-AzureProvisioningConfig** cmdlet.</span></span>
<span data-ttu-id="23001-108">Use um objeto de configuração para criar a máquina virtual usando o cmdlet **New-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="23001-108">Use a configuration object to create virtual machine by using the **New-AzureVM** cmdlet.</span></span>
<span data-ttu-id="23001-109">Você pode usar um objeto de configuração de certificado para criar uma máquina virtual usando o cmdlet **New-AzureQuickVM** .</span><span class="sxs-lookup"><span data-stu-id="23001-109">You can use a certificate setting object to create a virtual machine by using the **New-AzureQuickVM** cmdlet.</span></span>

## <span data-ttu-id="23001-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23001-110">EXAMPLES</span></span>

### <span data-ttu-id="23001-111">Exemplo 1: criar um objeto de configuração de certificado</span><span class="sxs-lookup"><span data-stu-id="23001-111">Example 1: Create a certificate setting object</span></span>
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

<span data-ttu-id="23001-112">Esse comando cria um objeto de configuração de certificado para um certificado existente.</span><span class="sxs-lookup"><span data-stu-id="23001-112">This command creates a certificate setting object for an existing certificate.</span></span>

### <span data-ttu-id="23001-113">Exemplo 2: criar uma máquina virtual que usa um objeto de configuração de configuração</span><span class="sxs-lookup"><span data-stu-id="23001-113">Example 2: Create a virtual machine that uses a configuration setting object</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="23001-114">O primeiro comando adiciona o certificado ContosoCert. cer ao serviço chamado ContosoService usando o cmdlet **Add-AzureCertificate** .</span><span class="sxs-lookup"><span data-stu-id="23001-114">The first command adds the certificate ContosoCert.cer to the service named ContosoService by using the **Add-AzureCertificate** cmdlet.</span></span>

<span data-ttu-id="23001-115">O segundo comando cria um objeto de configuração de certificado e, em seguida, armazena-o na variável $CertificateSetting.</span><span class="sxs-lookup"><span data-stu-id="23001-115">The second command creates a certificate setting object, and then stores it in the $CertificateSetting variable.</span></span>

<span data-ttu-id="23001-116">O terceiro comando obtém uma imagem do repositório de imagens usando o cmdlet **Get-AzureVMImage** .</span><span class="sxs-lookup"><span data-stu-id="23001-116">The third command gets an image from the image repository by using the **Get-AzureVMImage** cmdlet.</span></span>
<span data-ttu-id="23001-117">Esse comando armazena a imagem na variável $Image.</span><span class="sxs-lookup"><span data-stu-id="23001-117">This command store the image in the $Image variable.</span></span>

<span data-ttu-id="23001-118">O comando final cria um objeto de configuração de máquina virtual com base na imagem no $Image usando o cmdlet **New-AzureVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="23001-118">The final command creates a virtual machine configuration object based on the image in $Image by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="23001-119">O comando passa esse objeto para o cmdlet **Add-AzureProvisioningConfig** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="23001-119">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="23001-120">Esse cmdlet adiciona informações de provisionamento à configuração.</span><span class="sxs-lookup"><span data-stu-id="23001-120">That cmdlet add provisioning information to the configuration.</span></span>
<span data-ttu-id="23001-121">O comando passa o objeto para o cmdlet **New-AzureVM** , que cria a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="23001-121">The command passes the object to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

## <span data-ttu-id="23001-122">OS</span><span class="sxs-lookup"><span data-stu-id="23001-122">PARAMETERS</span></span>

### <span data-ttu-id="23001-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="23001-123">-InformationAction</span></span>
<span data-ttu-id="23001-124">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="23001-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="23001-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="23001-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23001-126">Contínuo</span><span class="sxs-lookup"><span data-stu-id="23001-126">Continue</span></span>
- <span data-ttu-id="23001-127">Ignorar</span><span class="sxs-lookup"><span data-stu-id="23001-127">Ignore</span></span>
- <span data-ttu-id="23001-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="23001-128">Inquire</span></span>
- <span data-ttu-id="23001-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="23001-129">SilentlyContinue</span></span>
- <span data-ttu-id="23001-130">Finaliza</span><span class="sxs-lookup"><span data-stu-id="23001-130">Stop</span></span>
- <span data-ttu-id="23001-131">Suspensão</span><span class="sxs-lookup"><span data-stu-id="23001-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23001-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="23001-132">-InformationVariable</span></span>
<span data-ttu-id="23001-133">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="23001-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23001-134">-StoreName</span><span class="sxs-lookup"><span data-stu-id="23001-134">-StoreName</span></span>
<span data-ttu-id="23001-135">Especifica o repositório de certificados no qual colocar o certificado.</span><span class="sxs-lookup"><span data-stu-id="23001-135">Specifies the certificate store in which to put the certificate.</span></span>
<span data-ttu-id="23001-136">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="23001-136">Valid values are:</span></span> 

- <span data-ttu-id="23001-137">Agenda</span><span class="sxs-lookup"><span data-stu-id="23001-137">AddressBook</span></span>
- <span data-ttu-id="23001-138">AuthRoot</span><span class="sxs-lookup"><span data-stu-id="23001-138">AuthRoot</span></span>
- <span data-ttu-id="23001-139">CertificateAuthority</span><span class="sxs-lookup"><span data-stu-id="23001-139">CertificateAuthority</span></span>
- <span data-ttu-id="23001-140">Não permitidas</span><span class="sxs-lookup"><span data-stu-id="23001-140">Disallowed</span></span>
- <span data-ttu-id="23001-141">Meu</span><span class="sxs-lookup"><span data-stu-id="23001-141">My</span></span>
- <span data-ttu-id="23001-142">Raiz</span><span class="sxs-lookup"><span data-stu-id="23001-142">Root</span></span>
- <span data-ttu-id="23001-143">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="23001-143">TrustedPeople</span></span>
- <span data-ttu-id="23001-144">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="23001-144">TrustedPublisher</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23001-145">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="23001-145">-Thumbprint</span></span>
<span data-ttu-id="23001-146">Especifica a impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="23001-146">Specifies the thumbprint of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23001-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23001-147">CommonParameters</span></span>
<span data-ttu-id="23001-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23001-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23001-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23001-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23001-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23001-150">INPUTS</span></span>

## <span data-ttu-id="23001-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23001-151">OUTPUTS</span></span>

## <span data-ttu-id="23001-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23001-152">NOTES</span></span>

## <span data-ttu-id="23001-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23001-153">RELATED LINKS</span></span>

[<span data-ttu-id="23001-154">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="23001-154">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="23001-155">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="23001-155">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="23001-156">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="23001-156">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="23001-157">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="23001-157">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="23001-158">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="23001-158">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)

[<span data-ttu-id="23001-159">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="23001-159">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="23001-160">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="23001-160">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


