---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: f1220db034a2cdcc81ffbd7a146fee8e2c7201be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599307"
---
# <span data-ttu-id="5c57f-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5c57f-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="5c57f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c57f-102">SYNOPSIS</span></span>
<span data-ttu-id="5c57f-103">Modifica um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="5c57f-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="5c57f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c57f-104">SYNTAX</span></span>

### <span data-ttu-id="5c57f-105">BySpecifiedScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="5c57f-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c57f-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5c57f-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c57f-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="5c57f-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c57f-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="5c57f-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c57f-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="5c57f-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c57f-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="5c57f-110">ByTenantLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c57f-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="5c57f-111">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c57f-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5c57f-112">DESCRIPTION</span></span>
<span data-ttu-id="5c57f-113">O cmdlet **set-AzResourceLock** modifica um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="5c57f-113">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="5c57f-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c57f-114">EXAMPLES</span></span>

### <span data-ttu-id="5c57f-115">Exemplo 1: atualizar notas para um bloqueio</span><span class="sxs-lookup"><span data-stu-id="5c57f-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="5c57f-116">Esse comando atualiza a anotação para um bloqueio chamado ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="5c57f-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="5c57f-117">OS</span><span class="sxs-lookup"><span data-stu-id="5c57f-117">PARAMETERS</span></span>

### <span data-ttu-id="5c57f-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5c57f-118">-ApiVersion</span></span>
<span data-ttu-id="5c57f-119">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="5c57f-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5c57f-120">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="5c57f-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5c57f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c57f-121">-DefaultProfile</span></span>
<span data-ttu-id="5c57f-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5c57f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c57f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="5c57f-123">-Force</span></span>
<span data-ttu-id="5c57f-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5c57f-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5c57f-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="5c57f-125">-LockId</span></span>
<span data-ttu-id="5c57f-126">Especifica a ID do bloqueio que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="5c57f-126">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5c57f-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="5c57f-127">-LockLevel</span></span>
<span data-ttu-id="5c57f-128">Especifica o nível para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="5c57f-128">Specifies the level for the lock.</span></span>
<span data-ttu-id="5c57f-129">Atualmente, o único valor válido é CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="5c57f-129">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="5c57f-130">-Lockname</span><span class="sxs-lookup"><span data-stu-id="5c57f-130">-LockName</span></span>
<span data-ttu-id="5c57f-131">Especifica o nome do bloqueio que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="5c57f-131">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c57f-132">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="5c57f-132">-LockNotes</span></span>
<span data-ttu-id="5c57f-133">Especifica as anotações para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="5c57f-133">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="5c57f-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="5c57f-134">-Pre</span></span>
<span data-ttu-id="5c57f-135">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="5c57f-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5c57f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c57f-136">-ResourceGroupName</span></span>
<span data-ttu-id="5c57f-137">Especifica o nome do grupo de recursos para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="5c57f-137">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="5c57f-138">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5c57f-138">-ResourceName</span></span>
<span data-ttu-id="5c57f-139">Especifica o nome do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="5c57f-139">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="5c57f-140">Por exemplo, para especificar um banco de dados, use o seguinte formato: banco de dados do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="5c57f-140">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c57f-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5c57f-141">-ResourceType</span></span>
<span data-ttu-id="5c57f-142">Especifica o tipo de recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="5c57f-142">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c57f-143">-Escopo</span><span class="sxs-lookup"><span data-stu-id="5c57f-143">-Scope</span></span>
<span data-ttu-id="5c57f-144">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="5c57f-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="5c57f-145">Por exemplo, para especificar um banco de dados, use o seguinte formato: nome `/subscriptions/` do grupo de recursos de ID de assinatura nome `/resourceGroups/` do nome `/providers/Microsoft.Sql/servers/` do grupo de recursos `/databases/` para especificar um grupo de recursos, use o seguinte formato: `/subscriptions/` nome do grupo de recursos de ID de assinatura `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="5c57f-145">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="5c57f-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="5c57f-146">-TenantLevel</span></span>
<span data-ttu-id="5c57f-147">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="5c57f-147">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c57f-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5c57f-148">-Confirm</span></span>
<span data-ttu-id="5c57f-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c57f-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c57f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c57f-150">-WhatIf</span></span>
<span data-ttu-id="5c57f-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5c57f-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c57f-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5c57f-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c57f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c57f-153">CommonParameters</span></span>
<span data-ttu-id="5c57f-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c57f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c57f-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c57f-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c57f-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5c57f-156">INPUTS</span></span>

### <span data-ttu-id="5c57f-157">System. String</span><span class="sxs-lookup"><span data-stu-id="5c57f-157">System.String</span></span>

### <span data-ttu-id="5c57f-158">Microsoft. Azure. Commands. ResourceManager. cmdlets. Entities. Locks. LockLevel</span><span class="sxs-lookup"><span data-stu-id="5c57f-158">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="5c57f-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5c57f-159">OUTPUTS</span></span>

### <span data-ttu-id="5c57f-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="5c57f-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5c57f-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5c57f-161">NOTES</span></span>

## <span data-ttu-id="5c57f-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c57f-162">RELATED LINKS</span></span>

[<span data-ttu-id="5c57f-163">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5c57f-163">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="5c57f-164">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5c57f-164">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="5c57f-165">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5c57f-165">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


