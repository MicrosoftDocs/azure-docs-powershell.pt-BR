---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: baff896564d8f3b8d70f69b190bc3429d4f465c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118658"
---
# <span data-ttu-id="36e85-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="36e85-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="36e85-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36e85-102">SYNOPSIS</span></span>
<span data-ttu-id="36e85-103">Adicione a extensão vm ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="36e85-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="36e85-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36e85-104">SYNTAX</span></span>

### <span data-ttu-id="36e85-105">ByObj (Padrão)</span><span class="sxs-lookup"><span data-stu-id="36e85-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36e85-106">ByName</span><span class="sxs-lookup"><span data-stu-id="36e85-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36e85-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="36e85-107">DESCRIPTION</span></span>
<span data-ttu-id="36e85-108">Adicione a extensão vm ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="36e85-108">Add vm extension to the node type.</span></span> <span data-ttu-id="36e85-109">Isso adicionará a extensão ao recurso Conjunto de Escala de Máquina Virtual sublimanal.</span><span class="sxs-lookup"><span data-stu-id="36e85-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="36e85-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="36e85-110">EXAMPLES</span></span>

### <span data-ttu-id="36e85-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="36e85-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="36e85-112">Esse comando adiciona uma extensão ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="36e85-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="36e85-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="36e85-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="36e85-114">Esse comando adiciona uma extensão com configurações e configurações protegidas ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="36e85-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="36e85-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="36e85-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="36e85-116">Esse comando adiciona uma extensão ao tipo de nó, com canos.</span><span class="sxs-lookup"><span data-stu-id="36e85-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="36e85-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36e85-117">PARAMETERS</span></span>

### <span data-ttu-id="36e85-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36e85-118">-AsJob</span></span>
<span data-ttu-id="36e85-119">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="36e85-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="36e85-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="36e85-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="36e85-121">Indica se a extensão deve usar uma versão secundária mais recente, se estiver disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="36e85-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="36e85-122">Uma vez implantada, no entanto, a extensão não atualizará as versões secundárias, a menos que seja reimplantada, mesmo com essa propriedade definida como verdadeira.</span><span class="sxs-lookup"><span data-stu-id="36e85-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="36e85-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="36e85-123">-ClusterName</span></span>
<span data-ttu-id="36e85-124">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="36e85-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="36e85-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e85-125">-DefaultProfile</span></span>
<span data-ttu-id="36e85-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36e85-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36e85-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="36e85-127">-ForceUpdateTag</span></span>
<span data-ttu-id="36e85-128">Se um valor for fornecido e for diferente do valor anterior, o manipulador de extensão será obrigado a atualizar mesmo que a configuração de extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="36e85-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="36e85-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36e85-129">-InputObject</span></span>
<span data-ttu-id="36e85-130">Recurso Tipo de Nó</span><span class="sxs-lookup"><span data-stu-id="36e85-130">Node Type resource</span></span>

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

### <span data-ttu-id="36e85-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="36e85-131">-Name</span></span>
<span data-ttu-id="36e85-132">nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="36e85-132">extension name.</span></span>

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

### <span data-ttu-id="36e85-133">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="36e85-133">-NodeTypeName</span></span>
<span data-ttu-id="36e85-134">Especifique o nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="36e85-134">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="36e85-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="36e85-135">-ProtectedSetting</span></span>
<span data-ttu-id="36e85-136">A extensão pode conterSettings protegidos ou protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="36e85-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="36e85-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="36e85-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="36e85-138">Conjunto de nomes de extensão após os quais essa extensão precisa ser provisionada.</span><span class="sxs-lookup"><span data-stu-id="36e85-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="36e85-139">-Publisher</span><span class="sxs-lookup"><span data-stu-id="36e85-139">-Publisher</span></span>
<span data-ttu-id="36e85-140">O nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="36e85-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="36e85-141">Isso pode usar o cmdlet Get-AzVMImagePublisher para obter o editor.</span><span class="sxs-lookup"><span data-stu-id="36e85-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="36e85-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36e85-142">-ResourceGroupName</span></span>
<span data-ttu-id="36e85-143">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="36e85-143">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="36e85-144">-Configuração</span><span class="sxs-lookup"><span data-stu-id="36e85-144">-Setting</span></span>
<span data-ttu-id="36e85-145">Json formatado configurações públicas para a extensão.</span><span class="sxs-lookup"><span data-stu-id="36e85-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="36e85-146">-Tipo</span><span class="sxs-lookup"><span data-stu-id="36e85-146">-Type</span></span>
<span data-ttu-id="36e85-147">Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="36e85-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="36e85-148">Você pode usar o cmdlet Get-AzVMExtensionImageType para obter o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="36e85-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="36e85-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="36e85-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="36e85-150">Especifica a versão do manipulador de script.</span><span class="sxs-lookup"><span data-stu-id="36e85-150">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="36e85-151">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="36e85-151">-Confirm</span></span>
<span data-ttu-id="36e85-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36e85-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36e85-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36e85-153">-WhatIf</span></span>
<span data-ttu-id="36e85-154">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="36e85-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36e85-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36e85-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36e85-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e85-156">CommonParameters</span></span>
<span data-ttu-id="36e85-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36e85-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e85-158">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36e85-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e85-159">Entradas</span><span class="sxs-lookup"><span data-stu-id="36e85-159">INPUTS</span></span>

### <span data-ttu-id="36e85-160">System.String</span><span class="sxs-lookup"><span data-stu-id="36e85-160">System.String</span></span>

### <span data-ttu-id="36e85-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="36e85-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="36e85-162">Saídas</span><span class="sxs-lookup"><span data-stu-id="36e85-162">OUTPUTS</span></span>

### <span data-ttu-id="36e85-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="36e85-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="36e85-164">Notas</span><span class="sxs-lookup"><span data-stu-id="36e85-164">NOTES</span></span>

## <span data-ttu-id="36e85-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36e85-165">RELATED LINKS</span></span>
