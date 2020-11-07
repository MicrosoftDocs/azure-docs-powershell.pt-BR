---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 97E9FB22-43A8-4D07-AF48-5884E4593CA9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f3baea7440d58812056999ea4f271acf80b8d4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945446"
---
# <span data-ttu-id="c0175-101">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="c0175-101">Set-AzureVMExtension</span></span>

## <span data-ttu-id="c0175-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0175-102">SYNOPSIS</span></span>
<span data-ttu-id="c0175-103">Define extensões de recursos para máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="c0175-103">Sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="c0175-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0175-104">SYNTAX</span></span>

### <span data-ttu-id="c0175-105">SetByExtensionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c0175-105">SetByExtensionName (Default)</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfiguration] <String>] [[-PrivateConfiguration] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0175-106">SetByExtensionNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="c0175-106">SetByExtensionNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0175-107">SetByReferenceName</span><span class="sxs-lookup"><span data-stu-id="c0175-107">SetByReferenceName</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfiguration] <String>]
 [[-PrivateConfiguration] <String>] [-Disable] [-Uninstall] [[-PublicConfigKey] <String>]
 [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c0175-108">SetByReferenceNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="c0175-108">SetByReferenceNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>]
 [-Disable] [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c0175-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c0175-109">DESCRIPTION</span></span>
<span data-ttu-id="c0175-110">O cmdlet **set-AzureVMExtension** define extensões de recursos para máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="c0175-110">The **Set-AzureVMExtension** cmdlet sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="c0175-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0175-111">EXAMPLES</span></span>

### <span data-ttu-id="c0175-112">Exemplo 1: criar uma máquina virtual com extensões de recursos aplicadas</span><span class="sxs-lookup"><span data-stu-id="c0175-112">Example 1: Create a virtual machine with resource extensions applied</span></span>
```
PS C:\> $X = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $IMG;$X = Add-AzureProvisioningConfig -VM $X -Password $PWD -AdminUsername $USR -Windows;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext1 -Publisher $Publisher -Version $VER -PublicConfiguration $P1 -PrivateConfiguration $P2;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext2 -Publisher $Publisher -Version $VER -PublicConfiguration $P3 -PrivateConfiguration $P4;New-AzureVM -Location $LOC -ServiceName $SVC -VM $X;
```

<span data-ttu-id="c0175-113">Esse comando cria uma máquina virtual com extensões de recurso aplicadas.</span><span class="sxs-lookup"><span data-stu-id="c0175-113">This command creates a virtual machine with resource extensions applied.</span></span>

## <span data-ttu-id="c0175-114">OS</span><span class="sxs-lookup"><span data-stu-id="c0175-114">PARAMETERS</span></span>

### <span data-ttu-id="c0175-115">-Disable</span><span class="sxs-lookup"><span data-stu-id="c0175-115">-Disable</span></span>
<span data-ttu-id="c0175-116">Indica que esse cmdlet desabilita o estado da extensão.</span><span class="sxs-lookup"><span data-stu-id="c0175-116">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0175-117">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="c0175-117">-ExtensionName</span></span>
<span data-ttu-id="c0175-118">Especifica o nome da extensão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c0175-118">Specifies the extension name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0175-119">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="c0175-119">-ForceUpdate</span></span>
<span data-ttu-id="c0175-120">Indica que esse cmdlet aplica novamente uma configuração a uma extensão quando a configuração não foi atualizada.</span><span class="sxs-lookup"><span data-stu-id="c0175-120">Indicates that this cmdlet re-applies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0175-121">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="c0175-121">-InformationAction</span></span>
<span data-ttu-id="c0175-122">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="c0175-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c0175-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c0175-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c0175-124">Contínuo</span><span class="sxs-lookup"><span data-stu-id="c0175-124">Continue</span></span>
- <span data-ttu-id="c0175-125">Ignorar</span><span class="sxs-lookup"><span data-stu-id="c0175-125">Ignore</span></span>
- <span data-ttu-id="c0175-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="c0175-126">Inquire</span></span>
- <span data-ttu-id="c0175-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c0175-127">SilentlyContinue</span></span>
- <span data-ttu-id="c0175-128">Finaliza</span><span class="sxs-lookup"><span data-stu-id="c0175-128">Stop</span></span>
- <span data-ttu-id="c0175-129">Suspensão</span><span class="sxs-lookup"><span data-stu-id="c0175-129">Suspend</span></span>

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

### <span data-ttu-id="c0175-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c0175-130">-InformationVariable</span></span>
<span data-ttu-id="c0175-131">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="c0175-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c0175-132">-PrivateConfigKey</span><span class="sxs-lookup"><span data-stu-id="c0175-132">-PrivateConfigKey</span></span>
<span data-ttu-id="c0175-133">Especifica uma chave de configuração privada.</span><span class="sxs-lookup"><span data-stu-id="c0175-133">Specifies a private configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0175-134">-PrivateConfigPath</span><span class="sxs-lookup"><span data-stu-id="c0175-134">-PrivateConfigPath</span></span>
<span data-ttu-id="c0175-135">Especifica o caminho de configuração particular.</span><span class="sxs-lookup"><span data-stu-id="c0175-135">Specifies the private configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0175-136">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0175-136">-PrivateConfiguration</span></span>
<span data-ttu-id="c0175-137">Especifica o texto de configuração particular.</span><span class="sxs-lookup"><span data-stu-id="c0175-137">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0175-138">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c0175-138">-Profile</span></span>
<span data-ttu-id="c0175-139">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c0175-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c0175-140">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c0175-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c0175-141">-PublicConfigKey</span><span class="sxs-lookup"><span data-stu-id="c0175-141">-PublicConfigKey</span></span>
<span data-ttu-id="c0175-142">Especifica a chave de configuração pública.</span><span class="sxs-lookup"><span data-stu-id="c0175-142">Specifies the public configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0175-143">-PublicConfigPath</span><span class="sxs-lookup"><span data-stu-id="c0175-143">-PublicConfigPath</span></span>
<span data-ttu-id="c0175-144">Especifica o caminho de configuração pública.</span><span class="sxs-lookup"><span data-stu-id="c0175-144">Specifies the public configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0175-145">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0175-145">-PublicConfiguration</span></span>
<span data-ttu-id="c0175-146">Especifica o texto de configuração pública.</span><span class="sxs-lookup"><span data-stu-id="c0175-146">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0175-147">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c0175-147">-Publisher</span></span>
<span data-ttu-id="c0175-148">Especifica o fornecedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="c0175-148">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0175-149">-Referencename</span><span class="sxs-lookup"><span data-stu-id="c0175-149">-ReferenceName</span></span>
<span data-ttu-id="c0175-150">Especifica o nome de referência da extensão.</span><span class="sxs-lookup"><span data-stu-id="c0175-150">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="c0175-151">Esta é uma cadeia de caracteres definida pelo usuário que pode ser usada para fazer referência a uma extensão.</span><span class="sxs-lookup"><span data-stu-id="c0175-151">This is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="c0175-152">Você precisa especificá-la quando a extensão for adicionada à máquina virtual pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="c0175-152">You need to specify it when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="c0175-153">Para atualizações subsequentes, você precisa especificar o nome de referência usado anteriormente ao atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="c0175-153">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="c0175-154">O Referencename atribuído a uma extensão é retornado usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="c0175-154">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByReferenceName, SetByReferenceNameAndConfigFile
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0175-155">-Desinstalar</span><span class="sxs-lookup"><span data-stu-id="c0175-155">-Uninstall</span></span>
<span data-ttu-id="c0175-156">Indica que esse cmdlet desinstala a extensão de recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c0175-156">Indicates that this cmdlet uninstalls the resource extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0175-157">-Versão</span><span class="sxs-lookup"><span data-stu-id="c0175-157">-Version</span></span>
<span data-ttu-id="c0175-158">Especifica a versão de extensão.</span><span class="sxs-lookup"><span data-stu-id="c0175-158">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0175-159">-VM</span><span class="sxs-lookup"><span data-stu-id="c0175-159">-VM</span></span>
<span data-ttu-id="c0175-160">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="c0175-160">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="c0175-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0175-161">CommonParameters</span></span>
<span data-ttu-id="c0175-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0175-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0175-163">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0175-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0175-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c0175-164">INPUTS</span></span>

## <span data-ttu-id="c0175-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c0175-165">OUTPUTS</span></span>

## <span data-ttu-id="c0175-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c0175-166">NOTES</span></span>

## <span data-ttu-id="c0175-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0175-167">RELATED LINKS</span></span>

[<span data-ttu-id="c0175-168">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="c0175-168">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="c0175-169">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="c0175-169">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="c0175-170">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c0175-170">Get-AzureVM</span></span>](./Get-AzureVM.md)


