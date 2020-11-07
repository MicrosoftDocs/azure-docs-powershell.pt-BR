---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945955"
---
# <span data-ttu-id="38abd-101">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="38abd-101">Set-AzurePublicIP</span></span>

## <span data-ttu-id="38abd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38abd-102">SYNOPSIS</span></span>
<span data-ttu-id="38abd-103">Adiciona um IP público a uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="38abd-103">Adds a Public IP to an Azure virtual machine.</span></span>

## <span data-ttu-id="38abd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38abd-104">SYNTAX</span></span>

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="38abd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38abd-105">DESCRIPTION</span></span>
<span data-ttu-id="38abd-106">O cmdlet **set-AzurePublicIP** adiciona um IP público a uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="38abd-106">The **Set-AzurePublicIP** cmdlet adds a Public IP to an Azure virtual machine.</span></span>
<span data-ttu-id="38abd-107">Se você executar esse cmdlet para uma máquina virtual existente, atualize a máquina virtual para implementá-las.</span><span class="sxs-lookup"><span data-stu-id="38abd-107">If you run this cmdlet for an existing virtual machine, update the virtual machine to implement your changes.</span></span>
<span data-ttu-id="38abd-108">Você pode especificar um rótulo de nome de domínio para criar uma entrada de DNS correspondente para o IP público.</span><span class="sxs-lookup"><span data-stu-id="38abd-108">You can specify a domain name label to create a corresponding DNS entry for the public IP.</span></span>

## <span data-ttu-id="38abd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38abd-109">EXAMPLES</span></span>

### <span data-ttu-id="38abd-110">Exemplo 1: adicionar um IP público a uma máquina virtual existente</span><span class="sxs-lookup"><span data-stu-id="38abd-110">Example 1: Add a Public IP to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

<span data-ttu-id="38abd-111">Esse comando obtém a máquina virtual chamada FTPInstance no serviço chamado FTPInAzure usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="38abd-111">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="38abd-112">O comando transmite a máquina virtual para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="38abd-112">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="38abd-113">O cmdlet atual adiciona a ftpip do nome do IP público.</span><span class="sxs-lookup"><span data-stu-id="38abd-113">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="38abd-114">O comando passa a máquina virtual para o cmdlet **Update-AzureVM** , que implementa suas alterações.</span><span class="sxs-lookup"><span data-stu-id="38abd-114">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="38abd-115">Exemplo 2: adicionar um IP público a uma nova máquina virtual</span><span class="sxs-lookup"><span data-stu-id="38abd-115">Example 2: Add a Public IP to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="38abd-116">Esse comando cria um objeto de configuração de máquina virtual usando o cmdlet **New-AzureVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="38abd-116">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="38abd-117">O comando passa esse objeto para o cmdlet **Add-AzureProvisioningConfig** , que fornece configuração adicional.</span><span class="sxs-lookup"><span data-stu-id="38abd-117">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet, which provides additional configuration.</span></span>
<span data-ttu-id="38abd-118">O cmdlet atual adiciona a ftpip do nome do IP público.</span><span class="sxs-lookup"><span data-stu-id="38abd-118">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="38abd-119">O comando passa a configuração para o cmdlet **New-AzureVM** , que cria a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="38abd-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="38abd-120">Exemplo 3: adicionar um IP público e um rótulo a uma máquina virtual existente</span><span class="sxs-lookup"><span data-stu-id="38abd-120">Example 3: Add a Public IP and label to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

<span data-ttu-id="38abd-121">Esse comando obtém a máquina virtual chamada FTPInstance no serviço chamado FTPInAzure usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="38abd-121">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="38abd-122">O comando transmite a máquina virtual para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="38abd-122">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="38abd-123">O cmdlet atual adiciona o ftpip de nomes de IP público e o rótulo ipname.</span><span class="sxs-lookup"><span data-stu-id="38abd-123">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="38abd-124">O comando atualiza a máquina virtual, que implementa suas alterações.</span><span class="sxs-lookup"><span data-stu-id="38abd-124">The command updates the virtual machine, which implements your changes.</span></span>

### <span data-ttu-id="38abd-125">Exemplo 4: adicionar um IP público e um rótulo a uma nova máquina virtual</span><span class="sxs-lookup"><span data-stu-id="38abd-125">Example 4: Add a Public IP and label to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="38abd-126">Esse comando cria um objeto de configuração de máquina virtual e, em seguida, passa esse objeto para **Add-AzureProvisioningConfig** , que fornece configuração adicional.</span><span class="sxs-lookup"><span data-stu-id="38abd-126">This command creates a virtual machine configuration object, and then passes that object to **Add-AzureProvisioningConfig** , which provides additional configuration.</span></span>
<span data-ttu-id="38abd-127">O cmdlet atual adiciona o ftpip de nomes de IP público e o rótulo ipname.</span><span class="sxs-lookup"><span data-stu-id="38abd-127">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="38abd-128">O comando cria a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="38abd-128">The command creates the virtual machine.</span></span>

## <span data-ttu-id="38abd-129">OS</span><span class="sxs-lookup"><span data-stu-id="38abd-129">PARAMETERS</span></span>

### <span data-ttu-id="38abd-130">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="38abd-130">-DomainNameLabel</span></span>
<span data-ttu-id="38abd-131">Especifica o nome a ser usado para uma entrada DNS correspondente para o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="38abd-131">Specifies the name to use for a corresponding DNS entry for the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38abd-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="38abd-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="38abd-133">Especifica o período de tempo limite de TCP ocioso em minutos.</span><span class="sxs-lookup"><span data-stu-id="38abd-133">Specifies the TCP idle time-out period in minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38abd-134">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="38abd-134">-InformationAction</span></span>
<span data-ttu-id="38abd-135">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="38abd-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="38abd-136">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="38abd-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="38abd-137">Contínuo</span><span class="sxs-lookup"><span data-stu-id="38abd-137">Continue</span></span>
- <span data-ttu-id="38abd-138">Ignorar</span><span class="sxs-lookup"><span data-stu-id="38abd-138">Ignore</span></span>
- <span data-ttu-id="38abd-139">Inquire</span><span class="sxs-lookup"><span data-stu-id="38abd-139">Inquire</span></span>
- <span data-ttu-id="38abd-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="38abd-140">SilentlyContinue</span></span>
- <span data-ttu-id="38abd-141">Finaliza</span><span class="sxs-lookup"><span data-stu-id="38abd-141">Stop</span></span>
- <span data-ttu-id="38abd-142">Suspensão</span><span class="sxs-lookup"><span data-stu-id="38abd-142">Suspend</span></span>

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

### <span data-ttu-id="38abd-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="38abd-143">-InformationVariable</span></span>
<span data-ttu-id="38abd-144">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="38abd-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="38abd-145">-Perfil</span><span class="sxs-lookup"><span data-stu-id="38abd-145">-Profile</span></span>
<span data-ttu-id="38abd-146">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="38abd-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="38abd-147">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="38abd-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38abd-148">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="38abd-148">-PublicIPName</span></span>
<span data-ttu-id="38abd-149">Especifica o nome do IP público.</span><span class="sxs-lookup"><span data-stu-id="38abd-149">Specifies the Public IP name.</span></span>

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

### <span data-ttu-id="38abd-150">-VM</span><span class="sxs-lookup"><span data-stu-id="38abd-150">-VM</span></span>
<span data-ttu-id="38abd-151">Especifica a máquina virtual para a qual esse cmdlet adiciona o IP público.</span><span class="sxs-lookup"><span data-stu-id="38abd-151">Specifies the virtual machine to which this cmdlet adds Public IP.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38abd-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38abd-152">CommonParameters</span></span>
<span data-ttu-id="38abd-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38abd-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38abd-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38abd-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38abd-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38abd-155">INPUTS</span></span>

## <span data-ttu-id="38abd-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38abd-156">OUTPUTS</span></span>

### <span data-ttu-id="38abd-157">Microsoft. WindowsAzure. Commands. onmanagement. Model. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="38abd-157">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="38abd-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38abd-158">NOTES</span></span>

## <span data-ttu-id="38abd-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38abd-159">RELATED LINKS</span></span>

[<span data-ttu-id="38abd-160">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="38abd-160">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="38abd-161">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="38abd-161">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="38abd-162">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="38abd-162">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="38abd-163">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="38abd-163">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="38abd-164">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="38abd-164">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="38abd-165">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="38abd-165">Update-AzureVM</span></span>](./Update-AzureVM.md)


