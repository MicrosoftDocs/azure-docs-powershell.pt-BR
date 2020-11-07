---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: fdf9f91570fc598806427b6812f52e397fb19322
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776313"
---
# <span data-ttu-id="14238-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="14238-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="14238-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14238-102">SYNOPSIS</span></span>
<span data-ttu-id="14238-103">Modifica um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="14238-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="14238-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14238-104">SYNTAX</span></span>

### <span data-ttu-id="14238-105">BySpecifiedScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="14238-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14238-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="14238-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14238-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="14238-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14238-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="14238-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14238-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="14238-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14238-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="14238-110">ByTenantLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14238-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="14238-111">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14238-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14238-112">DESCRIPTION</span></span>
<span data-ttu-id="14238-113">O cmdlet **set-AzResourceLock** modifica um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="14238-113">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="14238-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14238-114">EXAMPLES</span></span>

### <span data-ttu-id="14238-115">Exemplo 1: atualizar notas para um bloqueio</span><span class="sxs-lookup"><span data-stu-id="14238-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="14238-116">Esse comando atualiza a anotação para um bloqueio chamado ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="14238-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="14238-117">OS</span><span class="sxs-lookup"><span data-stu-id="14238-117">PARAMETERS</span></span>

### <span data-ttu-id="14238-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="14238-118">-ApiVersion</span></span>
<span data-ttu-id="14238-119">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="14238-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="14238-120">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="14238-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="14238-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14238-121">-DefaultProfile</span></span>
<span data-ttu-id="14238-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="14238-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14238-123">-Force</span><span class="sxs-lookup"><span data-stu-id="14238-123">-Force</span></span>
<span data-ttu-id="14238-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="14238-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="14238-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="14238-125">-InformationAction</span></span>
<span data-ttu-id="14238-126">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="14238-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="14238-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="14238-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14238-128">Contínuo</span><span class="sxs-lookup"><span data-stu-id="14238-128">Continue</span></span>
- <span data-ttu-id="14238-129">Ignorar</span><span class="sxs-lookup"><span data-stu-id="14238-129">Ignore</span></span>
- <span data-ttu-id="14238-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="14238-130">Inquire</span></span>
- <span data-ttu-id="14238-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="14238-131">SilentlyContinue</span></span>
- <span data-ttu-id="14238-132">Finaliza</span><span class="sxs-lookup"><span data-stu-id="14238-132">Stop</span></span>
- <span data-ttu-id="14238-133">Suspensão</span><span class="sxs-lookup"><span data-stu-id="14238-133">Suspend</span></span>

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

### <span data-ttu-id="14238-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="14238-134">-InformationVariable</span></span>
<span data-ttu-id="14238-135">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="14238-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="14238-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="14238-136">-LockId</span></span>
<span data-ttu-id="14238-137">Especifica a ID do bloqueio que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="14238-137">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="14238-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="14238-138">-LockLevel</span></span>
<span data-ttu-id="14238-139">Especifica o nível para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="14238-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="14238-140">Atualmente, o único valor válido é CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="14238-140">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="14238-141">-Lockname</span><span class="sxs-lookup"><span data-stu-id="14238-141">-LockName</span></span>
<span data-ttu-id="14238-142">Especifica o nome do bloqueio que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="14238-142">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="14238-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="14238-143">-LockNotes</span></span>
<span data-ttu-id="14238-144">Especifica as anotações para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="14238-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="14238-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="14238-145">-Pre</span></span>
<span data-ttu-id="14238-146">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="14238-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="14238-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14238-147">-ResourceGroupName</span></span>
<span data-ttu-id="14238-148">Especifica o nome do grupo de recursos para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="14238-148">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="14238-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="14238-149">-ResourceName</span></span>
<span data-ttu-id="14238-150">Especifica o nome do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="14238-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="14238-151">Por exemplo, para especificar um banco de dados, use o seguinte formato: banco de dados do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="14238-151">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="14238-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="14238-152">-ResourceType</span></span>
<span data-ttu-id="14238-153">Especifica o tipo de recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="14238-153">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="14238-154">-Escopo</span><span class="sxs-lookup"><span data-stu-id="14238-154">-Scope</span></span>
<span data-ttu-id="14238-155">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="14238-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="14238-156">Por exemplo, para especificar um banco de dados, use o seguinte formato: nome `/subscriptions/` do grupo de recursos de ID de assinatura nome `/resourceGroups/` do nome `/providers/Microsoft.Sql/servers/` do grupo de recursos `/databases/` para especificar um grupo de recursos, use o seguinte formato: `/subscriptions/` nome do grupo de recursos de ID de assinatura `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="14238-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="14238-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="14238-157">-TenantLevel</span></span>
<span data-ttu-id="14238-158">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="14238-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="14238-159">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14238-159">-Confirm</span></span>
<span data-ttu-id="14238-160">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14238-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14238-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14238-161">-WhatIf</span></span>
<span data-ttu-id="14238-162">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14238-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14238-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14238-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14238-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14238-164">CommonParameters</span></span>
<span data-ttu-id="14238-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14238-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14238-166">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14238-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14238-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14238-167">INPUTS</span></span>

## <span data-ttu-id="14238-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14238-168">OUTPUTS</span></span>

## <span data-ttu-id="14238-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14238-169">NOTES</span></span>

## <span data-ttu-id="14238-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14238-170">RELATED LINKS</span></span>

[<span data-ttu-id="14238-171">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="14238-171">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="14238-172">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="14238-172">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="14238-173">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="14238-173">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


