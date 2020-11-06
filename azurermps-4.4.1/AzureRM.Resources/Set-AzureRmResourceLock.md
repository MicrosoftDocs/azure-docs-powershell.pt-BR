---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
ms.openlocfilehash: 73d82366cc0120e057d0c083e7f6da0b3cdebb76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609565"
---
# <span data-ttu-id="3b406-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="3b406-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="3b406-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b406-102">SYNOPSIS</span></span>
<span data-ttu-id="3b406-103">Modifica um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="3b406-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b406-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b406-104">SYNTAX</span></span>

### <span data-ttu-id="3b406-105">Um bloqueio no escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="3b406-105">A lock at the specified scope.</span></span> <span data-ttu-id="3b406-106">Assume</span><span class="sxs-lookup"><span data-stu-id="3b406-106">(Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b406-107">Um bloqueio no escopo do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3b406-107">A lock at the resource group scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b406-108">Um bloqueio no escopo de recursos do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3b406-108">A lock at the resource group resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b406-109">Um bloqueio no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="3b406-109">A lock at the subscription scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b406-110">Um bloqueio no escopo do recurso de assinatura.</span><span class="sxs-lookup"><span data-stu-id="3b406-110">A lock at the subscription resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b406-111">Um bloqueio no escopo do recurso locatário.</span><span class="sxs-lookup"><span data-stu-id="3b406-111">A lock at the tenant resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b406-112">Um lock, por ID.</span><span class="sxs-lookup"><span data-stu-id="3b406-112">A lock, by Id.</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b406-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b406-113">DESCRIPTION</span></span>
<span data-ttu-id="3b406-114">O cmdlet **set-AzureRmResourceLock** modifica um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="3b406-114">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="3b406-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b406-115">EXAMPLES</span></span>

### <span data-ttu-id="3b406-116">Exemplo 1: atualizar notas para um bloqueio</span><span class="sxs-lookup"><span data-stu-id="3b406-116">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="3b406-117">Esse comando atualiza a anotação para um bloqueio chamado ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="3b406-117">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="3b406-118">OS</span><span class="sxs-lookup"><span data-stu-id="3b406-118">PARAMETERS</span></span>

### <span data-ttu-id="3b406-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3b406-119">-ApiVersion</span></span>
<span data-ttu-id="3b406-120">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="3b406-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3b406-121">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="3b406-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3b406-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3b406-122">-Force</span></span>
<span data-ttu-id="3b406-123">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3b406-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3b406-124">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="3b406-124">-InformationAction</span></span>
<span data-ttu-id="3b406-125">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="3b406-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3b406-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3b406-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3b406-127">Contínuo</span><span class="sxs-lookup"><span data-stu-id="3b406-127">Continue</span></span>
- <span data-ttu-id="3b406-128">Ignorar</span><span class="sxs-lookup"><span data-stu-id="3b406-128">Ignore</span></span>
- <span data-ttu-id="3b406-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="3b406-129">Inquire</span></span>
- <span data-ttu-id="3b406-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3b406-130">SilentlyContinue</span></span>
- <span data-ttu-id="3b406-131">Finaliza</span><span class="sxs-lookup"><span data-stu-id="3b406-131">Stop</span></span>
- <span data-ttu-id="3b406-132">Suspensão</span><span class="sxs-lookup"><span data-stu-id="3b406-132">Suspend</span></span>

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

### <span data-ttu-id="3b406-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3b406-133">-InformationVariable</span></span>
<span data-ttu-id="3b406-134">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="3b406-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3b406-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="3b406-135">-LockId</span></span>
<span data-ttu-id="3b406-136">Especifica a ID do bloqueio que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="3b406-136">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b406-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="3b406-137">-LockLevel</span></span>
<span data-ttu-id="3b406-138">Especifica o nível para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="3b406-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="3b406-139">Atualmente, o único valor válido é CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="3b406-139">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="3b406-140">-Lockname</span><span class="sxs-lookup"><span data-stu-id="3b406-140">-LockName</span></span>
<span data-ttu-id="3b406-141">Especifica o nome do bloqueio que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="3b406-141">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope., A lock at the resource group scope., A lock at the resource group resource scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b406-142">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="3b406-142">-LockNotes</span></span>
<span data-ttu-id="3b406-143">Especifica as anotações para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="3b406-143">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="3b406-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="3b406-144">-Pre</span></span>
<span data-ttu-id="3b406-145">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="3b406-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3b406-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b406-146">-ResourceGroupName</span></span>
<span data-ttu-id="3b406-147">Especifica o nome do grupo de recursos para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="3b406-147">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b406-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3b406-148">-ResourceName</span></span>
<span data-ttu-id="3b406-149">Especifica o nome do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="3b406-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="3b406-150">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="3b406-150">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="3b406-151">Banco de dados do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="3b406-151">Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b406-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="3b406-152">-ResourceType</span></span>
<span data-ttu-id="3b406-153">Especifica o tipo de recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="3b406-153">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b406-154">-Escopo</span><span class="sxs-lookup"><span data-stu-id="3b406-154">-Scope</span></span>
<span data-ttu-id="3b406-155">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="3b406-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="3b406-156">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="3b406-156">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="3b406-157">`/subscriptions/`ID `/resourceGroups/` do grupo de recursos nome do grupo nome `/providers/Microsoft.Sql/servers/` do `/databases/` banco de dados</span><span class="sxs-lookup"><span data-stu-id="3b406-157">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="3b406-158">Para especificar um grupo de recursos, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="3b406-158">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="3b406-159">`/subscriptions/`ID da assinatura `/resourceGroups/` nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3b406-159">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b406-160">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="3b406-160">-TenantLevel</span></span>
<span data-ttu-id="3b406-161">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="3b406-161">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b406-162">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3b406-162">-Confirm</span></span>
<span data-ttu-id="3b406-163">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b406-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b406-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b406-164">-WhatIf</span></span>
<span data-ttu-id="3b406-165">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3b406-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b406-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3b406-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b406-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b406-167">-DefaultProfile</span></span>
<span data-ttu-id="3b406-168">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b406-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b406-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b406-169">CommonParameters</span></span>
<span data-ttu-id="3b406-170">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b406-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b406-171">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b406-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b406-172">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b406-172">INPUTS</span></span>

## <span data-ttu-id="3b406-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b406-173">OUTPUTS</span></span>

### <span data-ttu-id="3b406-174">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3b406-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3b406-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b406-175">NOTES</span></span>

## <span data-ttu-id="3b406-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b406-176">RELATED LINKS</span></span>

[<span data-ttu-id="3b406-177">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="3b406-177">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="3b406-178">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="3b406-178">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="3b406-179">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="3b406-179">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)


