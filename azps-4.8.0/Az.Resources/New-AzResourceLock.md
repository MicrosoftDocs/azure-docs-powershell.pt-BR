---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 7f21704783a9992cc0d1b0fdf3da50cb21656b0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110967"
---
# <span data-ttu-id="8b3c7-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="8b3c7-101">New-AzResourceLock</span></span>

## <span data-ttu-id="8b3c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b3c7-102">SYNOPSIS</span></span>
<span data-ttu-id="8b3c7-103">Cria um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-103">Creates a resource lock.</span></span>

## <span data-ttu-id="8b3c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b3c7-104">SYNTAX</span></span>

### <span data-ttu-id="8b3c7-105">BySpecifiedScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="8b3c7-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b3c7-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b3c7-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b3c7-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="8b3c7-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b3c7-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="8b3c7-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b3c7-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="8b3c7-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b3c7-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="8b3c7-110">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b3c7-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b3c7-111">DESCRIPTION</span></span>
<span data-ttu-id="8b3c7-112">O cmdlet **New-AzResourceLock** cria um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-112">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="8b3c7-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b3c7-113">EXAMPLES</span></span>

### <span data-ttu-id="8b3c7-114">Exemplo 1: criar um bloqueio de recurso em um site</span><span class="sxs-lookup"><span data-stu-id="8b3c7-114">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="8b3c7-115">Esse comando cria um bloqueio de recurso em um site.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-115">This command creates a resource lock on a website.</span></span>

### <span data-ttu-id="8b3c7-116">Exemplo 2: criar um bloqueio de recurso em um banco de dados</span><span class="sxs-lookup"><span data-stu-id="8b3c7-116">Example 2: Create a resource lock on a database</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "Lock note" -LockName "db-lock" -ResourceName "server1/ContosoDB"  -ResourceGroupName "RG1" -ResourceType "Microsoft.Sql/servers/databases"
```

<span data-ttu-id="8b3c7-117">Esse comando cria um bloqueio de recurso em um banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-117">This command creates a resource lock on a Azure database.</span></span>

## <span data-ttu-id="8b3c7-118">OS</span><span class="sxs-lookup"><span data-stu-id="8b3c7-118">PARAMETERS</span></span>

### <span data-ttu-id="8b3c7-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8b3c7-119">-ApiVersion</span></span>
<span data-ttu-id="8b3c7-120">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8b3c7-121">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8b3c7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b3c7-122">-DefaultProfile</span></span>
<span data-ttu-id="8b3c7-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8b3c7-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b3c7-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8b3c7-124">-Force</span></span>
<span data-ttu-id="8b3c7-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b3c7-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="8b3c7-126">-LockId</span></span>
<span data-ttu-id="8b3c7-127">Especifica a ID do bloqueio.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-127">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="8b3c7-128">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="8b3c7-128">-LockLevel</span></span>
<span data-ttu-id="8b3c7-129">Especifica o nível para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-129">Specifies the level for the lock.</span></span>
<span data-ttu-id="8b3c7-130">Atualmente, os valores válidos são CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-130">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="8b3c7-131">-Lockname</span><span class="sxs-lookup"><span data-stu-id="8b3c7-131">-LockName</span></span>
<span data-ttu-id="8b3c7-132">Especifica o nome do bloqueio.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-132">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="8b3c7-133">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="8b3c7-133">-LockNotes</span></span>
<span data-ttu-id="8b3c7-134">Especifica as anotações para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-134">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="8b3c7-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="8b3c7-135">-Pre</span></span>
<span data-ttu-id="8b3c7-136">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8b3c7-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b3c7-137">-ResourceGroupName</span></span>
<span data-ttu-id="8b3c7-138">Especifica o nome de um grupo de recursos para o qual o bloqueio se aplica ou que contém o grupo de recursos ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-138">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="8b3c7-139">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8b3c7-139">-ResourceName</span></span>
<span data-ttu-id="8b3c7-140">Especifica o nome do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-140">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="8b3c7-141">Por exemplo, para especificar um banco de dados, use o seguinte formato: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="8b3c7-141">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="8b3c7-142">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8b3c7-142">-ResourceType</span></span>
<span data-ttu-id="8b3c7-143">Especifica o tipo de recurso do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-143">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="8b3c7-144">-Escopo</span><span class="sxs-lookup"><span data-stu-id="8b3c7-144">-Scope</span></span>
<span data-ttu-id="8b3c7-145">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-145">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="8b3c7-146">Por exemplo, para especificar um banco de dados, use o seguinte formato: nome `/subscriptions/` do grupo de recursos de ID de assinatura nome `/resourceGroups/` do nome `/providers/Microsoft.Sql/servers/` do grupo de recursos `/databases/` para especificar um grupo de recursos, use o seguinte formato: `/subscriptions/` nome do grupo de recursos de ID de assinatura `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="8b3c7-146">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="8b3c7-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8b3c7-147">-Confirm</span></span>
<span data-ttu-id="8b3c7-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b3c7-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b3c7-149">-WhatIf</span></span>
<span data-ttu-id="8b3c7-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b3c7-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b3c7-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b3c7-152">CommonParameters</span></span>
<span data-ttu-id="8b3c7-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b3c7-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b3c7-154">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b3c7-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b3c7-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b3c7-155">INPUTS</span></span>

### <span data-ttu-id="8b3c7-156">System. String</span><span class="sxs-lookup"><span data-stu-id="8b3c7-156">System.String</span></span>

### <span data-ttu-id="8b3c7-157">Microsoft. Azure. Commands. ResourceManager. cmdlets. Entities. Locks. LockLevel</span><span class="sxs-lookup"><span data-stu-id="8b3c7-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="8b3c7-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b3c7-158">OUTPUTS</span></span>

### <span data-ttu-id="8b3c7-159">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8b3c7-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8b3c7-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b3c7-160">NOTES</span></span>

## <span data-ttu-id="8b3c7-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b3c7-161">RELATED LINKS</span></span>

[<span data-ttu-id="8b3c7-162">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="8b3c7-162">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="8b3c7-163">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="8b3c7-163">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="8b3c7-164">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="8b3c7-164">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


