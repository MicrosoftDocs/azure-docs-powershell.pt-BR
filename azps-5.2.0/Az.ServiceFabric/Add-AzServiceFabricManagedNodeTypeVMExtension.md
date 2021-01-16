---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: baff896564d8f3b8d70f69b190bc3429d4f465c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260816"
---
# <span data-ttu-id="a505d-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="a505d-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="a505d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a505d-102">SYNOPSIS</span></span>
<span data-ttu-id="a505d-103">Adicionar extensão de VM ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="a505d-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="a505d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a505d-104">SYNTAX</span></span>

### <span data-ttu-id="a505d-105">ByObj (padrão)</span><span class="sxs-lookup"><span data-stu-id="a505d-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a505d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a505d-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a505d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a505d-107">DESCRIPTION</span></span>
<span data-ttu-id="a505d-108">Adicionar extensão de VM ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="a505d-108">Add vm extension to the node type.</span></span> <span data-ttu-id="a505d-109">Isso adicionará a extensão ao recurso do conjunto de escala da máquina virtual underliying.</span><span class="sxs-lookup"><span data-stu-id="a505d-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="a505d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a505d-110">EXAMPLES</span></span>

### <span data-ttu-id="a505d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a505d-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="a505d-112">Esse comando adiciona uma extensão ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="a505d-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="a505d-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a505d-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="a505d-114">Esse comando adiciona uma extensão com configurações e configurações protegidas ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="a505d-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="a505d-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a505d-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="a505d-116">Esse comando adiciona uma extensão ao tipo de nó, com tubulação.</span><span class="sxs-lookup"><span data-stu-id="a505d-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="a505d-117">OS</span><span class="sxs-lookup"><span data-stu-id="a505d-117">PARAMETERS</span></span>

### <span data-ttu-id="a505d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a505d-118">-AsJob</span></span>
<span data-ttu-id="a505d-119">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="a505d-119">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a505d-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a505d-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a505d-121">Indica se a extensão deve usar uma versão secundária mais recente, se disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="a505d-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="a505d-122">Depois de implantada, no entanto, a extensão não atualizará versões secundárias, a menos que reimplantada, mesmo com essa propriedade definida como true.</span><span class="sxs-lookup"><span data-stu-id="a505d-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a505d-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a505d-123">-ClusterName</span></span>
<span data-ttu-id="a505d-124">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="a505d-124">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a505d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a505d-125">-DefaultProfile</span></span>
<span data-ttu-id="a505d-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a505d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a505d-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="a505d-127">-ForceUpdateTag</span></span>
<span data-ttu-id="a505d-128">Se um valor for fornecido e for diferente do valor anterior, o manipulador de extensão será forçado a atualizar mesmo que a configuração de extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="a505d-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a505d-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a505d-129">-InputObject</span></span>
<span data-ttu-id="a505d-130">Recurso de tipo de nó</span><span class="sxs-lookup"><span data-stu-id="a505d-130">Node Type resource</span></span>

```yaml
Type: PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a505d-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="a505d-131">-Name</span></span>
<span data-ttu-id="a505d-132">nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="a505d-132">extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a505d-133">-NodeTypename</span><span class="sxs-lookup"><span data-stu-id="a505d-133">-NodeTypeName</span></span>
<span data-ttu-id="a505d-134">Especifique o nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="a505d-134">Specify the name of the node type.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a505d-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="a505d-135">-ProtectedSetting</span></span>
<span data-ttu-id="a505d-136">A extensão pode conter o protectedSettings ou o protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="a505d-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a505d-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="a505d-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="a505d-138">Coleção de nomes de extensão após o qual essa extensão precisa ser provisionada.</span><span class="sxs-lookup"><span data-stu-id="a505d-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a505d-139">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a505d-139">-Publisher</span></span>
<span data-ttu-id="a505d-140">O nome do fornecedor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="a505d-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="a505d-141">Isso pode usar o cmdlet Get-AzVMImagePublisher para obter o fornecedor.</span><span class="sxs-lookup"><span data-stu-id="a505d-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a505d-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a505d-142">-ResourceGroupName</span></span>
<span data-ttu-id="a505d-143">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a505d-143">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a505d-144">-Configuração</span><span class="sxs-lookup"><span data-stu-id="a505d-144">-Setting</span></span>
<span data-ttu-id="a505d-145">Configurações públicas formatadas como JSON para a extensão.</span><span class="sxs-lookup"><span data-stu-id="a505d-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a505d-146">-Digite</span><span class="sxs-lookup"><span data-stu-id="a505d-146">-Type</span></span>
<span data-ttu-id="a505d-147">Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="a505d-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="a505d-148">Você pode usar o cmdlet Get-AzVMExtensionImageType para obter o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="a505d-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a505d-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a505d-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="a505d-150">Especifica a versão do manipulador de script.</span><span class="sxs-lookup"><span data-stu-id="a505d-150">Specifies the version of the script handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a505d-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a505d-151">-Confirm</span></span>
<span data-ttu-id="a505d-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a505d-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a505d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a505d-153">-WhatIf</span></span>
<span data-ttu-id="a505d-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a505d-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a505d-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a505d-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a505d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a505d-156">CommonParameters</span></span>
<span data-ttu-id="a505d-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a505d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a505d-158">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a505d-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a505d-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a505d-159">INPUTS</span></span>

### <span data-ttu-id="a505d-160">System. String</span><span class="sxs-lookup"><span data-stu-id="a505d-160">System.String</span></span>

### <span data-ttu-id="a505d-161">Microsoft. Azure. Commands. imfabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="a505d-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="a505d-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a505d-162">OUTPUTS</span></span>

### <span data-ttu-id="a505d-163">Microsoft. Azure. Commands. imfabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="a505d-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="a505d-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a505d-164">NOTES</span></span>

## <span data-ttu-id="a505d-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a505d-165">RELATED LINKS</span></span>
