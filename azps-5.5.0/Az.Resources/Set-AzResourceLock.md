---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: c532633de593294c6b5dbe0e09b9615a1d5355a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111407"
---
# <span data-ttu-id="c76b2-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c76b2-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="c76b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c76b2-102">SYNOPSIS</span></span>
<span data-ttu-id="c76b2-103">Modifica um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="c76b2-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="c76b2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c76b2-104">SYNTAX</span></span>

### <span data-ttu-id="c76b2-105">BySpecifiedScope (Default)</span><span class="sxs-lookup"><span data-stu-id="c76b2-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c76b2-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c76b2-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c76b2-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="c76b2-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c76b2-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="c76b2-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c76b2-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="c76b2-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c76b2-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="c76b2-110">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c76b2-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c76b2-111">DESCRIPTION</span></span>
<span data-ttu-id="c76b2-112">O **cmdlet Set-AzResourceLock** modifica um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="c76b2-112">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="c76b2-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c76b2-113">EXAMPLES</span></span>

### <span data-ttu-id="c76b2-114">Exemplo 1: Atualizar anotações para um bloqueio</span><span class="sxs-lookup"><span data-stu-id="c76b2-114">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="c76b2-115">Este comando atualiza a anotação de um bloqueio chamado ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="c76b2-115">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="c76b2-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c76b2-116">PARAMETERS</span></span>

### <span data-ttu-id="c76b2-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c76b2-117">-ApiVersion</span></span>
<span data-ttu-id="c76b2-118">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="c76b2-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c76b2-119">Se você não especificar uma versão, este cmdlet usará a versão disponível mais recente.</span><span class="sxs-lookup"><span data-stu-id="c76b2-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c76b2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c76b2-120">-DefaultProfile</span></span>
<span data-ttu-id="c76b2-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c76b2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c76b2-122">-Forçar</span><span class="sxs-lookup"><span data-stu-id="c76b2-122">-Force</span></span>
<span data-ttu-id="c76b2-123">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c76b2-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c76b2-124">-LockId</span><span class="sxs-lookup"><span data-stu-id="c76b2-124">-LockId</span></span>
<span data-ttu-id="c76b2-125">Especifica a ID do bloqueio que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="c76b2-125">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76b2-126">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="c76b2-126">-LockLevel</span></span>
<span data-ttu-id="c76b2-127">Especifica o nível do bloqueio.</span><span class="sxs-lookup"><span data-stu-id="c76b2-127">Specifies the level for the lock.</span></span>
<span data-ttu-id="c76b2-128">Atualmente, o único valor válido é CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="c76b2-128">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76b2-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="c76b2-129">-LockName</span></span>
<span data-ttu-id="c76b2-130">Especifica o nome do bloqueio que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="c76b2-130">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76b2-131">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="c76b2-131">-LockNotes</span></span>
<span data-ttu-id="c76b2-132">Especifica as anotações do bloqueio.</span><span class="sxs-lookup"><span data-stu-id="c76b2-132">Specifies the notes for the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76b2-133">-Pré-</span><span class="sxs-lookup"><span data-stu-id="c76b2-133">-Pre</span></span>
<span data-ttu-id="c76b2-134">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="c76b2-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c76b2-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c76b2-135">-ResourceGroupName</span></span>
<span data-ttu-id="c76b2-136">Especifica o nome do grupo de recursos para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="c76b2-136">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76b2-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c76b2-137">-ResourceName</span></span>
<span data-ttu-id="c76b2-138">Especifica o nome do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="c76b2-138">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="c76b2-139">Por exemplo, para especificar um banco de dados, use o seguinte formato: Banco de Dados do `/` Servidor</span><span class="sxs-lookup"><span data-stu-id="c76b2-139">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76b2-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c76b2-140">-ResourceType</span></span>
<span data-ttu-id="c76b2-141">Especifica o tipo de recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="c76b2-141">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76b2-142">-Escopo</span><span class="sxs-lookup"><span data-stu-id="c76b2-142">-Scope</span></span>
<span data-ttu-id="c76b2-143">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="c76b2-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="c76b2-144">Por exemplo, para especificar um banco de dados, use o seguinte formato: nome do banco de dados de nome do servidor de nome do grupo de recursos de ID de assinatura Para especificar um grupo de recursos, use o seguinte formato: nome do grupo de recursos `/subscriptions/` `/resourceGroups/` de `/providers/Microsoft.Sql/servers/` `/databases/` `/subscriptions/` ID `/resourceGroups/` de assinatura</span><span class="sxs-lookup"><span data-stu-id="c76b2-144">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76b2-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c76b2-145">-Confirm</span></span>
<span data-ttu-id="c76b2-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c76b2-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c76b2-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c76b2-147">-WhatIf</span></span>
<span data-ttu-id="c76b2-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c76b2-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c76b2-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c76b2-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c76b2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c76b2-150">CommonParameters</span></span>
<span data-ttu-id="c76b2-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c76b2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c76b2-152">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c76b2-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c76b2-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="c76b2-153">INPUTS</span></span>

### <span data-ttu-id="c76b2-154">System.String</span><span class="sxs-lookup"><span data-stu-id="c76b2-154">System.String</span></span>

### <span data-ttu-id="c76b2-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span><span class="sxs-lookup"><span data-stu-id="c76b2-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="c76b2-156">Saídas</span><span class="sxs-lookup"><span data-stu-id="c76b2-156">OUTPUTS</span></span>

### <span data-ttu-id="c76b2-157">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="c76b2-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c76b2-158">Notas</span><span class="sxs-lookup"><span data-stu-id="c76b2-158">NOTES</span></span>

## <span data-ttu-id="c76b2-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c76b2-159">RELATED LINKS</span></span>

[<span data-ttu-id="c76b2-160">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c76b2-160">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="c76b2-161">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c76b2-161">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="c76b2-162">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c76b2-162">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


