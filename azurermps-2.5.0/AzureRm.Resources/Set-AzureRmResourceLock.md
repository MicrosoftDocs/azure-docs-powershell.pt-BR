---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: ccb491742d9a66a7e6eb300d7e75be0dcfac687e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785143"
---
# <span data-ttu-id="b6cd2-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="b6cd2-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="b6cd2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="b6cd2-103">Modifica um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6cd2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6cd2-104">SYNTAX</span></span>

### <span data-ttu-id="b6cd2-105">BySpecifiedScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="b6cd2-105">BySpecifiedScope (Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6cd2-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b6cd2-106">ByResourceGroup</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6cd2-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="b6cd2-107">ByResourceGroupLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6cd2-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="b6cd2-108">BySubscription</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6cd2-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="b6cd2-109">BySubscriptionLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6cd2-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="b6cd2-110">ByTenantLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6cd2-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="b6cd2-111">ByLockId</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6cd2-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6cd2-112">DESCRIPTION</span></span>
<span data-ttu-id="b6cd2-113">O cmdlet **set-AzureRmResourceLock** modifica um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-113">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="b6cd2-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6cd2-114">EXAMPLES</span></span>

### <span data-ttu-id="b6cd2-115">Exemplo 1: atualizar notas para um bloqueio</span><span class="sxs-lookup"><span data-stu-id="b6cd2-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="b6cd2-116">Esse comando atualiza a anotação para um bloqueio chamado ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="b6cd2-117">OS</span><span class="sxs-lookup"><span data-stu-id="b6cd2-117">PARAMETERS</span></span>

### <span data-ttu-id="b6cd2-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b6cd2-118">-ApiVersion</span></span>
<span data-ttu-id="b6cd2-119">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b6cd2-120">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b6cd2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6cd2-121">-DefaultProfile</span></span>
<span data-ttu-id="b6cd2-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b6cd2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cd2-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b6cd2-123">-Force</span></span>
<span data-ttu-id="b6cd2-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b6cd2-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b6cd2-125">-InformationAction</span></span>
<span data-ttu-id="b6cd2-126">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="b6cd2-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b6cd2-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b6cd2-128">Contínuo</span><span class="sxs-lookup"><span data-stu-id="b6cd2-128">Continue</span></span>
- <span data-ttu-id="b6cd2-129">Ignorar</span><span class="sxs-lookup"><span data-stu-id="b6cd2-129">Ignore</span></span>
- <span data-ttu-id="b6cd2-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="b6cd2-130">Inquire</span></span>
- <span data-ttu-id="b6cd2-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b6cd2-131">SilentlyContinue</span></span>
- <span data-ttu-id="b6cd2-132">Finaliza</span><span class="sxs-lookup"><span data-stu-id="b6cd2-132">Stop</span></span>
- <span data-ttu-id="b6cd2-133">Suspensão</span><span class="sxs-lookup"><span data-stu-id="b6cd2-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cd2-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b6cd2-134">-InformationVariable</span></span>
<span data-ttu-id="b6cd2-135">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cd2-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="b6cd2-136">-LockId</span></span>
<span data-ttu-id="b6cd2-137">Especifica a ID do bloqueio que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-137">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b6cd2-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="b6cd2-138">-LockLevel</span></span>
<span data-ttu-id="b6cd2-139">Especifica o nível para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="b6cd2-140">Atualmente, o único valor válido é CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-140">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cd2-141">-Lockname</span><span class="sxs-lookup"><span data-stu-id="b6cd2-141">-LockName</span></span>
<span data-ttu-id="b6cd2-142">Especifica o nome do bloqueio que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-142">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b6cd2-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="b6cd2-143">-LockNotes</span></span>
<span data-ttu-id="b6cd2-144">Especifica as anotações para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="b6cd2-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="b6cd2-145">-Pre</span></span>
<span data-ttu-id="b6cd2-146">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b6cd2-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6cd2-147">-ResourceGroupName</span></span>
<span data-ttu-id="b6cd2-148">Especifica o nome do grupo de recursos para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-148">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="b6cd2-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b6cd2-149">-ResourceName</span></span>
<span data-ttu-id="b6cd2-150">Especifica o nome do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="b6cd2-151">Por exemplo, para especificar um banco de dados, use o seguinte formato: banco de dados do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="b6cd2-151">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="b6cd2-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b6cd2-152">-ResourceType</span></span>
<span data-ttu-id="b6cd2-153">Especifica o tipo de recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-153">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="b6cd2-154">-Escopo</span><span class="sxs-lookup"><span data-stu-id="b6cd2-154">-Scope</span></span>
<span data-ttu-id="b6cd2-155">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="b6cd2-156">Por exemplo, para especificar um banco de dados, use o seguinte formato: nome `/subscriptions/` do grupo de recursos de ID de assinatura nome `/resourceGroups/` do nome `/providers/Microsoft.Sql/servers/` do grupo de recursos `/databases/` para especificar um grupo de recursos, use o seguinte formato: `/subscriptions/` nome do grupo de recursos de ID de assinatura `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="b6cd2-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="b6cd2-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="b6cd2-157">-TenantLevel</span></span>
<span data-ttu-id="b6cd2-158">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="b6cd2-159">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b6cd2-159">-Confirm</span></span>
<span data-ttu-id="b6cd2-160">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6cd2-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6cd2-161">-WhatIf</span></span>
<span data-ttu-id="b6cd2-162">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6cd2-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6cd2-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6cd2-164">CommonParameters</span></span>
<span data-ttu-id="b6cd2-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6cd2-166">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6cd2-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6cd2-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6cd2-167">INPUTS</span></span>

## <span data-ttu-id="b6cd2-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6cd2-168">OUTPUTS</span></span>

## <span data-ttu-id="b6cd2-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6cd2-169">NOTES</span></span>

## <span data-ttu-id="b6cd2-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6cd2-170">RELATED LINKS</span></span>

[<span data-ttu-id="b6cd2-171">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="b6cd2-171">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="b6cd2-172">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="b6cd2-172">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="b6cd2-173">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="b6cd2-173">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)


