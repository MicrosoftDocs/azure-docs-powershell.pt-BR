---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
ms.openlocfilehash: 12d1a696bd37cd6844a54f32f60bf70eaba6a0b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433427"
---
# <span data-ttu-id="06f29-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="06f29-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="06f29-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06f29-102">SYNOPSIS</span></span>
<span data-ttu-id="06f29-103">Modifica um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="06f29-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06f29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06f29-104">SYNTAX</span></span>

### <span data-ttu-id="06f29-105">BySpecifiedScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="06f29-105">BySpecifiedScope (Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06f29-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="06f29-106">ByResourceGroup</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06f29-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="06f29-107">ByResourceGroupLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06f29-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="06f29-108">BySubscription</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06f29-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="06f29-109">BySubscriptionLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06f29-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="06f29-110">ByTenantLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06f29-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="06f29-111">ByLockId</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06f29-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06f29-112">DESCRIPTION</span></span>
<span data-ttu-id="06f29-113">O cmdlet **set-AzureRmResourceLock** modifica um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="06f29-113">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="06f29-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06f29-114">EXAMPLES</span></span>

### <span data-ttu-id="06f29-115">Exemplo 1: atualizar notas para um bloqueio</span><span class="sxs-lookup"><span data-stu-id="06f29-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="06f29-116">Esse comando atualiza a anotação para um bloqueio chamado ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="06f29-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="06f29-117">OS</span><span class="sxs-lookup"><span data-stu-id="06f29-117">PARAMETERS</span></span>

### <span data-ttu-id="06f29-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="06f29-118">-ApiVersion</span></span>
<span data-ttu-id="06f29-119">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="06f29-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="06f29-120">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="06f29-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="06f29-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06f29-121">-DefaultProfile</span></span>
<span data-ttu-id="06f29-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="06f29-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06f29-123">-Force</span><span class="sxs-lookup"><span data-stu-id="06f29-123">-Force</span></span>
<span data-ttu-id="06f29-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="06f29-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="06f29-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="06f29-125">-InformationAction</span></span>
<span data-ttu-id="06f29-126">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="06f29-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="06f29-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="06f29-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06f29-128">Contínuo</span><span class="sxs-lookup"><span data-stu-id="06f29-128">Continue</span></span>
- <span data-ttu-id="06f29-129">Ignorar</span><span class="sxs-lookup"><span data-stu-id="06f29-129">Ignore</span></span>
- <span data-ttu-id="06f29-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="06f29-130">Inquire</span></span>
- <span data-ttu-id="06f29-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="06f29-131">SilentlyContinue</span></span>
- <span data-ttu-id="06f29-132">Finaliza</span><span class="sxs-lookup"><span data-stu-id="06f29-132">Stop</span></span>
- <span data-ttu-id="06f29-133">Suspensão</span><span class="sxs-lookup"><span data-stu-id="06f29-133">Suspend</span></span>

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

### <span data-ttu-id="06f29-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="06f29-134">-InformationVariable</span></span>
<span data-ttu-id="06f29-135">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="06f29-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="06f29-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="06f29-136">-LockId</span></span>
<span data-ttu-id="06f29-137">Especifica a ID do bloqueio que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="06f29-137">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06f29-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="06f29-138">-LockLevel</span></span>
<span data-ttu-id="06f29-139">Especifica o nível para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="06f29-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="06f29-140">Atualmente, o único valor válido é CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="06f29-140">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06f29-141">-Lockname</span><span class="sxs-lookup"><span data-stu-id="06f29-141">-LockName</span></span>
<span data-ttu-id="06f29-142">Especifica o nome do bloqueio que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="06f29-142">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06f29-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="06f29-143">-LockNotes</span></span>
<span data-ttu-id="06f29-144">Especifica as anotações para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="06f29-144">Specifies the notes for the lock.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06f29-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="06f29-145">-Pre</span></span>
<span data-ttu-id="06f29-146">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="06f29-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="06f29-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06f29-147">-ResourceGroupName</span></span>
<span data-ttu-id="06f29-148">Especifica o nome do grupo de recursos para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="06f29-148">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06f29-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="06f29-149">-ResourceName</span></span>
<span data-ttu-id="06f29-150">Especifica o nome do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="06f29-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="06f29-151">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="06f29-151">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="06f29-152">Banco de dados do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="06f29-152">Server`/`Database</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06f29-153">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="06f29-153">-ResourceType</span></span>
<span data-ttu-id="06f29-154">Especifica o tipo de recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="06f29-154">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06f29-155">-Escopo</span><span class="sxs-lookup"><span data-stu-id="06f29-155">-Scope</span></span>
<span data-ttu-id="06f29-156">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="06f29-156">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="06f29-157">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="06f29-157">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="06f29-158">`/subscriptions/`ID `/resourceGroups/` do grupo de recursos nome do grupo nome `/providers/Microsoft.Sql/servers/` do `/databases/` banco de dados</span><span class="sxs-lookup"><span data-stu-id="06f29-158">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="06f29-159">Para especificar um grupo de recursos, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="06f29-159">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="06f29-160">`/subscriptions/`ID da assinatura `/resourceGroups/` nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="06f29-160">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06f29-161">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="06f29-161">-TenantLevel</span></span>
<span data-ttu-id="06f29-162">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="06f29-162">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06f29-163">-Confirme</span><span class="sxs-lookup"><span data-stu-id="06f29-163">-Confirm</span></span>
<span data-ttu-id="06f29-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06f29-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06f29-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06f29-165">-WhatIf</span></span>
<span data-ttu-id="06f29-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="06f29-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06f29-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="06f29-167">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06f29-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06f29-168">CommonParameters</span></span>
<span data-ttu-id="06f29-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06f29-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06f29-170">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06f29-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06f29-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06f29-171">INPUTS</span></span>

### <span data-ttu-id="06f29-172">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="06f29-172">None</span></span>
<span data-ttu-id="06f29-173">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="06f29-173">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06f29-174">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06f29-174">OUTPUTS</span></span>

### <span data-ttu-id="06f29-175">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="06f29-175">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="06f29-176">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06f29-176">NOTES</span></span>

## <span data-ttu-id="06f29-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06f29-177">RELATED LINKS</span></span>

[<span data-ttu-id="06f29-178">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="06f29-178">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="06f29-179">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="06f29-179">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="06f29-180">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="06f29-180">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)


