---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AA58B897-EFA0-4321-9246-ED8E11AB3538
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a0e0d5cac7ac27bf7eeefe8e3eb995a82a32ea4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945982"
---
# <span data-ttu-id="7a1d2-101">New-AzureSSHKey</span><span class="sxs-lookup"><span data-stu-id="7a1d2-101">New-AzureSSHKey</span></span>

## <span data-ttu-id="7a1d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a1d2-102">SYNOPSIS</span></span>
<span data-ttu-id="7a1d2-103">Cria um objeto chave SSH para inserir um certificado existente em uma nova máquina virtual do Azure com base em Linux.</span><span class="sxs-lookup"><span data-stu-id="7a1d2-103">Creates a SSH Key object to insert an existing certificate into a new Linux-based Azure virtual machines.</span></span>

## <span data-ttu-id="7a1d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a1d2-104">SYNTAX</span></span>

### <span data-ttu-id="7a1d2-105">par de chaves</span><span class="sxs-lookup"><span data-stu-id="7a1d2-105">keypair</span></span>
```
New-AzureSSHKey [-KeyPair] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7a1d2-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="7a1d2-106">publickey</span></span>
```
New-AzureSSHKey [-PublicKey] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7a1d2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a1d2-107">DESCRIPTION</span></span>
<span data-ttu-id="7a1d2-108">O cmdlet **New-AzureSSHKey** cria um objeto chave SSH para um certificado que já foi adicionado ao Azure.</span><span class="sxs-lookup"><span data-stu-id="7a1d2-108">The **New-AzureSSHKey** cmdlet creates an SSH Key object for a certificate that has already been added to Azure.</span></span>
<span data-ttu-id="7a1d2-109">Esse objeto chave SSH pode ser usado por **New-AzureProvisioningConfig** ao criar o objeto de configuração para uma nova máquina virtual usando **New-AzureVM** ou ao criar uma nova máquina virtual com **New-AzureQuickVM**.</span><span class="sxs-lookup"><span data-stu-id="7a1d2-109">This SSH Key object can then be used by **New-AzureProvisioningConfig** when creating the configuration object for a new virtual machine using **New-AzureVM** , or when creating a new virtual machine with **New-AzureQuickVM**.</span></span>
<span data-ttu-id="7a1d2-110">Quando incluída como parte de um script de criação de máquina virtual, isso adiciona a chave pública SSH ou par de chaves especificado à nova máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7a1d2-110">When included as part of a virtual machine creation script, this adds the specified SSH Public Key or Key Pair to the new virtual machine.</span></span>

## <span data-ttu-id="7a1d2-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a1d2-111">EXAMPLES</span></span>

### <span data-ttu-id="7a1d2-112">Exemplo 1: criar um objeto de configuração de certificado</span><span class="sxs-lookup"><span data-stu-id="7a1d2-112">Example 1: Create a certificate setting object</span></span>
```
PS C:\> $myLxCert = New-AzureSSHKey -Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
```

<span data-ttu-id="7a1d2-113">Esse comando cria um objeto de configuração de certificado para um certificado existente e, em seguida, armazena o objeto em uma variável para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="7a1d2-113">This command creates a certificate setting object for an existing certificate and then stores the object in a variable for later use.</span></span>

### <span data-ttu-id="7a1d2-114">Exemplo 2: adicionar um certificado a um serviço</span><span class="sxs-lookup"><span data-stu-id="7a1d2-114">Example 2: Add a certificate to a service</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "MySvc" -CertToDeploy "C:\temp\MyLxCert.cer"
$myLxCert = New-AzureSSHKey ?Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
New-AzureVMConfig -Name "MyVM2" -InstanceSize Small -ImageName $LxImage `
          | Add-AzureProvisioningConfig -Linux -LinuxUser $lxUser -SSHPublicKeys $myLxCert -Password 'pass@word1' `
          | New-AzureVM -ServiceName "MySvc"
```

<span data-ttu-id="7a1d2-115">Esse comando adiciona um certificado a um serviço do Azure e, em seguida, cria uma nova máquina virtual Linux que usa o certificado.</span><span class="sxs-lookup"><span data-stu-id="7a1d2-115">This command adds a certificate to an Azure service, and then creates a new Linux virtual machine that uses the certificate.</span></span>

## <span data-ttu-id="7a1d2-116">OS</span><span class="sxs-lookup"><span data-stu-id="7a1d2-116">PARAMETERS</span></span>

### <span data-ttu-id="7a1d2-117">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="7a1d2-117">-Fingerprint</span></span>
<span data-ttu-id="7a1d2-118">Especifica a impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="7a1d2-118">Specifies the fingerprint of the certificate.</span></span>

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

### <span data-ttu-id="7a1d2-119">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="7a1d2-119">-InformationAction</span></span>
<span data-ttu-id="7a1d2-120">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="7a1d2-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7a1d2-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7a1d2-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7a1d2-122">Contínuo</span><span class="sxs-lookup"><span data-stu-id="7a1d2-122">Continue</span></span>
- <span data-ttu-id="7a1d2-123">Ignorar</span><span class="sxs-lookup"><span data-stu-id="7a1d2-123">Ignore</span></span>
- <span data-ttu-id="7a1d2-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="7a1d2-124">Inquire</span></span>
- <span data-ttu-id="7a1d2-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7a1d2-125">SilentlyContinue</span></span>
- <span data-ttu-id="7a1d2-126">Finaliza</span><span class="sxs-lookup"><span data-stu-id="7a1d2-126">Stop</span></span>
- <span data-ttu-id="7a1d2-127">Suspensão</span><span class="sxs-lookup"><span data-stu-id="7a1d2-127">Suspend</span></span>

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

### <span data-ttu-id="7a1d2-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7a1d2-128">-InformationVariable</span></span>
<span data-ttu-id="7a1d2-129">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="7a1d2-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7a1d2-130">-Par de chaves</span><span class="sxs-lookup"><span data-stu-id="7a1d2-130">-KeyPair</span></span>
<span data-ttu-id="7a1d2-131">Especifica que esse cmdlet cria um objeto para a inserção de um par de chaves SSH na nova configuração de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7a1d2-131">Specifies that this cmdlet creates an object for inserting an SSH Key Pair into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: keypair
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1d2-132">-Caminho</span><span class="sxs-lookup"><span data-stu-id="7a1d2-132">-Path</span></span>
<span data-ttu-id="7a1d2-133">Especifica o caminho para armazenar a chave pública SSH ou par de chaves.</span><span class="sxs-lookup"><span data-stu-id="7a1d2-133">Specifies the path to store the SSH Public Key or Key Pair.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1d2-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="7a1d2-134">-PublicKey</span></span>
<span data-ttu-id="7a1d2-135">Especifica que esse cmdlet cria um objeto para a inserção de uma chave pública SSH na nova configuração de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7a1d2-135">Specifies that this cmdlet creates an object for inserting an SSH Public Key into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: publickey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1d2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a1d2-136">CommonParameters</span></span>
<span data-ttu-id="7a1d2-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a1d2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a1d2-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a1d2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a1d2-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a1d2-139">INPUTS</span></span>

## <span data-ttu-id="7a1d2-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a1d2-140">OUTPUTS</span></span>

## <span data-ttu-id="7a1d2-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a1d2-141">NOTES</span></span>

## <span data-ttu-id="7a1d2-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a1d2-142">RELATED LINKS</span></span>

[<span data-ttu-id="7a1d2-143">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="7a1d2-143">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="7a1d2-144">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="7a1d2-144">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="7a1d2-145">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="7a1d2-145">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="7a1d2-146">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="7a1d2-146">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


