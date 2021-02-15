---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 22dfee058a26163206c973f664615a4f29ae61de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112073"
---
# <span data-ttu-id="21f91-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="21f91-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="21f91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21f91-102">SYNOPSIS</span></span>
<span data-ttu-id="21f91-103">Atualiza um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="21f91-103">Updates a container registry.</span></span>

## <span data-ttu-id="21f91-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21f91-104">SYNTAX</span></span>

### <span data-ttu-id="21f91-105">NameResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="21f91-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21f91-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="21f91-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21f91-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="21f91-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21f91-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21f91-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21f91-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21f91-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21f91-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21f91-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21f91-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="21f91-111">DESCRIPTION</span></span>
<span data-ttu-id="21f91-112">O Update-AzContainerRegistry cmdlet atualiza um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="21f91-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="21f91-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="21f91-113">EXAMPLES</span></span>

### <span data-ttu-id="21f91-114">Exemplo 1: Habilitar o usuário de administrador para um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="21f91-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="21f91-115">Esse comando habilita o usuário de administrador para o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="21f91-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="21f91-116">Exemplo 2: Definir a conta de armazenamento usada por um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="21f91-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="21f91-117">Esse comando define o registro de contêiner especificado para usar uma conta de armazenamento existente \` mystorageaccount \` na mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="21f91-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="21f91-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21f91-118">PARAMETERS</span></span>

### <span data-ttu-id="21f91-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21f91-119">-DefaultProfile</span></span>
<span data-ttu-id="21f91-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="21f91-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21f91-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="21f91-121">-DisableAdminUser</span></span>
<span data-ttu-id="21f91-122">Habilitar o usuário administrador para o registro de contêineres.</span><span class="sxs-lookup"><span data-stu-id="21f91-122">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f91-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="21f91-123">-EnableAdminUser</span></span>
<span data-ttu-id="21f91-124">Habilitar o usuário administrador para o registro de contêineres.</span><span class="sxs-lookup"><span data-stu-id="21f91-124">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f91-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="21f91-125">-Name</span></span>
<span data-ttu-id="21f91-126">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="21f91-126">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f91-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="21f91-127">-NetworkRuleSet</span></span>
<span data-ttu-id="21f91-128">A regra de rede definida para um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="21f91-128">The network rule set for a container registry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f91-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21f91-129">-ResourceGroupName</span></span>
<span data-ttu-id="21f91-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="21f91-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f91-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21f91-131">-ResourceId</span></span>
<span data-ttu-id="21f91-132">A ID do recurso de registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="21f91-132">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f91-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="21f91-133">-Sku</span></span>
<span data-ttu-id="21f91-134">SKU do Registro de Contêineres.</span><span class="sxs-lookup"><span data-stu-id="21f91-134">Container Registry SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f91-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="21f91-135">-StorageAccountName</span></span>
<span data-ttu-id="21f91-136">O nome de uma conta de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="21f91-136">The name of an existing storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f91-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="21f91-137">-Tag</span></span>
<span data-ttu-id="21f91-138">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="21f91-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="21f91-139">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="21f91-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f91-140">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="21f91-140">-Confirm</span></span>
<span data-ttu-id="21f91-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21f91-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f91-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21f91-142">-WhatIf</span></span>
<span data-ttu-id="21f91-143">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="21f91-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21f91-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21f91-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f91-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21f91-145">CommonParameters</span></span>
<span data-ttu-id="21f91-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21f91-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21f91-147">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21f91-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21f91-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="21f91-148">INPUTS</span></span>

### <span data-ttu-id="21f91-149">System.String</span><span class="sxs-lookup"><span data-stu-id="21f91-149">System.String</span></span>

## <span data-ttu-id="21f91-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="21f91-150">OUTPUTS</span></span>

### <span data-ttu-id="21f91-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="21f91-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="21f91-152">Notas</span><span class="sxs-lookup"><span data-stu-id="21f91-152">NOTES</span></span>

## <span data-ttu-id="21f91-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21f91-153">RELATED LINKS</span></span>

[<span data-ttu-id="21f91-154">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="21f91-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="21f91-155">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="21f91-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="21f91-156">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="21f91-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

