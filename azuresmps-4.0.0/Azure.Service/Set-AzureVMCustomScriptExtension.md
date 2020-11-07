---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A8F07D1-AC20-4950-9019-BDFB4FD3CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7569e203369bf1177b4eecc2bd689f3e20dcd48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946037"
---
# <span data-ttu-id="270a3-101">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="270a3-101">Set-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="270a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="270a3-102">SYNOPSIS</span></span>
<span data-ttu-id="270a3-103">Define informações para uma extensão de script personalizado da máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="270a3-103">Sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="270a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="270a3-104">SYNTAX</span></span>

### <span data-ttu-id="270a3-105">SetCustomScriptExtensionByContainerAndFileNames (padrão)</span><span class="sxs-lookup"><span data-stu-id="270a3-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-ContainerName] <String>
 [-FileName] <String[]> [[-StorageAccountName] <String>] [[-StorageEndpointSuffix] <String>]
 [[-StorageAccountKey] <String>] [[-Run] <String>] [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="270a3-106">DisableCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="270a3-106">DisableCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="270a3-107">UninstalleCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="270a3-107">UninstalleCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="270a3-108">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="270a3-108">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [[-FileUri] <String[]>]
 [-Run] <String> [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="270a3-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="270a3-109">DESCRIPTION</span></span>
<span data-ttu-id="270a3-110">O cmdlet **set-AzureVMCustomScriptExtension** define informações para uma extensão de script personalizado da máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="270a3-110">The **Set-AzureVMCustomScriptExtension** cmdlet sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="270a3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="270a3-111">EXAMPLES</span></span>

### <span data-ttu-id="270a3-112">Exemplo 1: definir informações para uma extensão de script personalizado da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="270a3-112">Example 1: Set information for a virtual machine custom script extension</span></span>
```
PS C:\> $VM = Set-AzureVMCustomScriptExtension -VM $VM -ContainerName "Container01" -FileName "script1.ps1","script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> New-AzureVM -Location "West US" -ServiceName $SVC -VM $VM;
```

<span data-ttu-id="270a3-113">Este comando define informações para uma extensão de script personalizado da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="270a3-113">This command sets information for a virtual machine custom script extension.</span></span>

### <span data-ttu-id="270a3-114">Exemplo 2: definir informações para uma extensão de script personalizada de máquina virtual usando um caminho de arquivo</span><span class="sxs-lookup"><span data-stu-id="270a3-114">Example 2: Set information for a virtual machine custom script extension using a file path</span></span>
```
PS C:\> Set-AzureVMCustomScriptExtension -VM $VM -FileUri "http://www.blob.core.contoso.net/bar/script1.ps1","http://www.blob.core.contoso.net/baz/script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> Update-AzureVM -ServiceName $SVC -Name $Name -VM VM;
```

<span data-ttu-id="270a3-115">Este comando define informações para uma extensão de script personalizado da máquina virtual usando várias URLs de arquivo.</span><span class="sxs-lookup"><span data-stu-id="270a3-115">This command sets information for a virtual machine custom script extension using multiple file URLs.</span></span>

## <span data-ttu-id="270a3-116">OS</span><span class="sxs-lookup"><span data-stu-id="270a3-116">PARAMETERS</span></span>

### <span data-ttu-id="270a3-117">-Argumento</span><span class="sxs-lookup"><span data-stu-id="270a3-117">-Argument</span></span>
<span data-ttu-id="270a3-118">Especifica uma cadeia de caracteres que fornece um argumento que este cmdlet executa na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="270a3-118">Specifies a string that supplies an argument that this cmdlet runs on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames, SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270a3-119">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="270a3-119">-ContainerName</span></span>
<span data-ttu-id="270a3-120">Especifica o nome do contêiner na conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="270a3-120">Specifies the container name within the storage account.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270a3-121">-Disable</span><span class="sxs-lookup"><span data-stu-id="270a3-121">-Disable</span></span>
<span data-ttu-id="270a3-122">Indica que esse cmdlet desabilita o estado da extensão.</span><span class="sxs-lookup"><span data-stu-id="270a3-122">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270a3-123">-Nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="270a3-123">-FileName</span></span>
<span data-ttu-id="270a3-124">Especifica uma matriz de cadeia de caracteres que contém os nomes dos arquivos blob no contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="270a3-124">Specifies a string array that contains the names of the blob files in the specified container.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270a3-125">-FileUri</span><span class="sxs-lookup"><span data-stu-id="270a3-125">-FileUri</span></span>
<span data-ttu-id="270a3-126">Especifica uma matriz de cadeia de caracteres que contém as URLs dos arquivos BLOB.</span><span class="sxs-lookup"><span data-stu-id="270a3-126">Specifies a string array that contains the URLs of the blob files.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270a3-127">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="270a3-127">-ForceUpdate</span></span>
<span data-ttu-id="270a3-128">Indica que esse cmdlet aplica novamente uma configuração a uma extensão quando a configuração não foi atualizada.</span><span class="sxs-lookup"><span data-stu-id="270a3-128">Indicates that this cmdlet re-apply a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="270a3-129">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="270a3-129">-InformationAction</span></span>
<span data-ttu-id="270a3-130">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="270a3-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="270a3-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="270a3-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="270a3-132">Contínuo</span><span class="sxs-lookup"><span data-stu-id="270a3-132">Continue</span></span>
- <span data-ttu-id="270a3-133">Ignorar</span><span class="sxs-lookup"><span data-stu-id="270a3-133">Ignore</span></span>
- <span data-ttu-id="270a3-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="270a3-134">Inquire</span></span>
- <span data-ttu-id="270a3-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="270a3-135">SilentlyContinue</span></span>
- <span data-ttu-id="270a3-136">Finaliza</span><span class="sxs-lookup"><span data-stu-id="270a3-136">Stop</span></span>
- <span data-ttu-id="270a3-137">Suspensão</span><span class="sxs-lookup"><span data-stu-id="270a3-137">Suspend</span></span>

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

### <span data-ttu-id="270a3-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="270a3-138">-InformationVariable</span></span>
<span data-ttu-id="270a3-139">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="270a3-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="270a3-140">-Perfil</span><span class="sxs-lookup"><span data-stu-id="270a3-140">-Profile</span></span>
<span data-ttu-id="270a3-141">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="270a3-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="270a3-142">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="270a3-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="270a3-143">-Referencename</span><span class="sxs-lookup"><span data-stu-id="270a3-143">-ReferenceName</span></span>
<span data-ttu-id="270a3-144">Especifica o nome de referência para a extensão.</span><span class="sxs-lookup"><span data-stu-id="270a3-144">Specifies the reference name for the extension.</span></span>

<span data-ttu-id="270a3-145">Esse parâmetro é uma cadeia de caracteres definida pelo usuário que pode ser usada para fazer referência a uma extensão.</span><span class="sxs-lookup"><span data-stu-id="270a3-145">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="270a3-146">Ele é especificado quando a extensão é adicionada à máquina virtual pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="270a3-146">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="270a3-147">Para atualizações subsequentes, você precisa especificar o nome de referência usado anteriormente ao atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="270a3-147">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="270a3-148">O *referencename* atribuído a uma extensão é retornado usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="270a3-148">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270a3-149">-Executar</span><span class="sxs-lookup"><span data-stu-id="270a3-149">-Run</span></span>
<span data-ttu-id="270a3-150">Especifica o comando que esse cmdlet executa pela extensão na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="270a3-150">Specifies the command this cmdlet runs by the extension on the virtual machine.</span></span>
<span data-ttu-id="270a3-151">Só há suporte para "powershell.exe".</span><span class="sxs-lookup"><span data-stu-id="270a3-151">Only "powershell.exe" is supported.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: RunFile, Command

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: RunFile, Command

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270a3-152">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="270a3-152">-StorageAccountKey</span></span>
<span data-ttu-id="270a3-153">Especifica a chave da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="270a3-153">Specifies the storage account key</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270a3-154">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="270a3-154">-StorageAccountName</span></span>
<span data-ttu-id="270a3-155">Especifica o nome da conta de armazenamento na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="270a3-155">Specifies the storage account name in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270a3-156">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="270a3-156">-StorageEndpointSuffix</span></span>
<span data-ttu-id="270a3-157">Especifica o ponto de extremidade do serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="270a3-157">Specifies the storage service endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270a3-158">-Desinstalar</span><span class="sxs-lookup"><span data-stu-id="270a3-158">-Uninstall</span></span>
<span data-ttu-id="270a3-159">Indica que esse cmdlet desinstala a extensão de script personalizada da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="270a3-159">Indicates that this cmdlet uninstalls the custom script extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstalleCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270a3-160">-Versão</span><span class="sxs-lookup"><span data-stu-id="270a3-160">-Version</span></span>
<span data-ttu-id="270a3-161">Especifica a versão da extensão de script personalizada.</span><span class="sxs-lookup"><span data-stu-id="270a3-161">Specifies the version of the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270a3-162">-VM</span><span class="sxs-lookup"><span data-stu-id="270a3-162">-VM</span></span>
<span data-ttu-id="270a3-163">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="270a3-163">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="270a3-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="270a3-164">CommonParameters</span></span>
<span data-ttu-id="270a3-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="270a3-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="270a3-166">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="270a3-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="270a3-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="270a3-167">INPUTS</span></span>

## <span data-ttu-id="270a3-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="270a3-168">OUTPUTS</span></span>

## <span data-ttu-id="270a3-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="270a3-169">NOTES</span></span>

## <span data-ttu-id="270a3-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="270a3-170">RELATED LINKS</span></span>

[<span data-ttu-id="270a3-171">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="270a3-171">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="270a3-172">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="270a3-172">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="270a3-173">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="270a3-173">Get-AzureVM</span></span>](./Get-AzureVM.md)


