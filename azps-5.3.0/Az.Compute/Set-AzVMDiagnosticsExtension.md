---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 5705d899f06d4a834b8864ec2a66c268e1c99c84
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434188"
---
# <span data-ttu-id="98d53-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="98d53-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="98d53-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98d53-102">SYNOPSIS</span></span>
<span data-ttu-id="98d53-103">Configura a extensão de diagnóstico do Azure em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="98d53-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="98d53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98d53-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98d53-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98d53-105">DESCRIPTION</span></span>
<span data-ttu-id="98d53-106">O cmdlet **set-AzVMDiagnosticsExtension** configura a extensão de diagnóstico do Azure em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="98d53-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="98d53-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98d53-107">EXAMPLES</span></span>

### <span data-ttu-id="98d53-108">Exemplo 1: habilitar o diagnóstico usando uma conta de armazenamento especificada em um arquivo de configuração de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="98d53-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="98d53-109">Esse comando usa um arquivo de configuração de diagnóstico para habilitar o diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="98d53-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="98d53-110">O arquivo diagnostics_publicconfig.xml contém a configuração de XML público para a extensão do diagnóstico, incluindo o nome da conta de armazenamento à qual os dados de diagnóstico serão enviados.</span><span class="sxs-lookup"><span data-stu-id="98d53-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="98d53-111">A conta de armazenamento de diagnóstico deve estar na mesma assinatura que a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="98d53-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="98d53-112">Exemplo 2: habilitar o diagnóstico usando um nome de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="98d53-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="98d53-113">Esse comando usa o nome da conta de armazenamento para habilitar o diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="98d53-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="98d53-114">Se a configuração de diagnóstico não especificar um nome de conta de armazenamento ou se você quiser substituir o nome da conta de armazenamento de diagnóstico especificado no arquivo de configuração, use o parâmetro *StorageAccountName* .</span><span class="sxs-lookup"><span data-stu-id="98d53-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="98d53-115">A conta de armazenamento de diagnóstico deve estar na mesma assinatura que a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="98d53-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="98d53-116">Exemplo 3: habilitar o diagnóstico usando o nome e a chave da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="98d53-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="98d53-117">Esse comando usa o nome da conta de armazenamento e a chave para habilitar o diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="98d53-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="98d53-118">Se a conta de armazenamento de diagnóstico estiver em uma assinatura diferente da máquina virtual, então habilite o envio de dados de diagnóstico para essa conta de armazenamento especificando explicitamente seu nome e chave.</span><span class="sxs-lookup"><span data-stu-id="98d53-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="98d53-119">OS</span><span class="sxs-lookup"><span data-stu-id="98d53-119">PARAMETERS</span></span>

### <span data-ttu-id="98d53-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="98d53-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="98d53-121">Indica se esse cmdlet permite que o agente convidado do Azure atualize automaticamente a extensão para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="98d53-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98d53-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98d53-122">-DefaultProfile</span></span>
<span data-ttu-id="98d53-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98d53-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98d53-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="98d53-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="98d53-125">Especifica o caminho do arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="98d53-125">Specifies the path of the configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98d53-126">-Local</span><span class="sxs-lookup"><span data-stu-id="98d53-126">-Location</span></span>
<span data-ttu-id="98d53-127">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="98d53-127">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98d53-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="98d53-128">-Name</span></span>
<span data-ttu-id="98d53-129">Especifica o nome de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="98d53-129">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98d53-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="98d53-130">-NoWait</span></span>
<span data-ttu-id="98d53-131">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="98d53-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="98d53-132">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="98d53-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98d53-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98d53-133">-ResourceGroupName</span></span>
<span data-ttu-id="98d53-134">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="98d53-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98d53-135">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="98d53-135">-StorageAccountEndpoint</span></span>
<span data-ttu-id="98d53-136">Especifica o ponto de extremidade da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="98d53-136">Specifies the storage account endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98d53-137">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="98d53-137">-StorageAccountKey</span></span>
<span data-ttu-id="98d53-138">Especifica a chave da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="98d53-138">Specifies the storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98d53-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="98d53-139">-StorageAccountName</span></span>
<span data-ttu-id="98d53-140">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="98d53-140">Specifies the storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98d53-141">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="98d53-141">-StorageContext</span></span>
<span data-ttu-id="98d53-142">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="98d53-142">Specifies the Azure storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98d53-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="98d53-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="98d53-144">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="98d53-144">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="98d53-145">Para obter a versão, execute o cmdlet Get-AzVMExtensionImage com um valor de Microsoft. COMPUTE para o parâmetro *PublisherName* e VMAccessAgent para o parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="98d53-145">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98d53-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="98d53-146">-VMName</span></span>
<span data-ttu-id="98d53-147">Especifica o nome da máquina virtual na qual esse cmdlet funciona.</span><span class="sxs-lookup"><span data-stu-id="98d53-147">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98d53-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d53-148">CommonParameters</span></span>
<span data-ttu-id="98d53-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98d53-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d53-150">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98d53-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d53-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98d53-151">INPUTS</span></span>

### <span data-ttu-id="98d53-152">System. String</span><span class="sxs-lookup"><span data-stu-id="98d53-152">System.String</span></span>

### <span data-ttu-id="98d53-153">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="98d53-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="98d53-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="98d53-154">System.Boolean</span></span>

## <span data-ttu-id="98d53-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98d53-155">OUTPUTS</span></span>

### <span data-ttu-id="98d53-156">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="98d53-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="98d53-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98d53-157">NOTES</span></span>

## <span data-ttu-id="98d53-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98d53-158">RELATED LINKS</span></span>

[<span data-ttu-id="98d53-159">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="98d53-159">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="98d53-160">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="98d53-160">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="98d53-161">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="98d53-161">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)


