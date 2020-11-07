---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 8d4f4180cc827c879dde0252044d30d5242d2300
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776384"
---
# <span data-ttu-id="9c002-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="9c002-101">New-AzResourceLock</span></span>

## <span data-ttu-id="9c002-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c002-102">SYNOPSIS</span></span>
<span data-ttu-id="9c002-103">Cria um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="9c002-103">Creates a resource lock.</span></span>

## <span data-ttu-id="9c002-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c002-104">SYNTAX</span></span>

### <span data-ttu-id="9c002-105">BySpecifiedScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="9c002-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c002-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9c002-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c002-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="9c002-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c002-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="9c002-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c002-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="9c002-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c002-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="9c002-110">ByTenantLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c002-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="9c002-111">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c002-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c002-112">DESCRIPTION</span></span>
<span data-ttu-id="9c002-113">O cmdlet **New-AzResourceLock** cria um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="9c002-113">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="9c002-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c002-114">EXAMPLES</span></span>

### <span data-ttu-id="9c002-115">Exemplo 1: criar um bloqueio de recurso em um site</span><span class="sxs-lookup"><span data-stu-id="9c002-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="9c002-116">Esse comando cria um bloqueio de recurso em um site.</span><span class="sxs-lookup"><span data-stu-id="9c002-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="9c002-117">OS</span><span class="sxs-lookup"><span data-stu-id="9c002-117">PARAMETERS</span></span>

### <span data-ttu-id="9c002-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9c002-118">-ApiVersion</span></span>
<span data-ttu-id="9c002-119">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="9c002-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9c002-120">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="9c002-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9c002-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c002-121">-DefaultProfile</span></span>
<span data-ttu-id="9c002-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9c002-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c002-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9c002-123">-Force</span></span>
<span data-ttu-id="9c002-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="9c002-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9c002-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="9c002-125">-InformationAction</span></span>
<span data-ttu-id="9c002-126">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="9c002-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="9c002-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9c002-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9c002-128">Contínuo</span><span class="sxs-lookup"><span data-stu-id="9c002-128">Continue</span></span>
- <span data-ttu-id="9c002-129">Ignorar</span><span class="sxs-lookup"><span data-stu-id="9c002-129">Ignore</span></span>
- <span data-ttu-id="9c002-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="9c002-130">Inquire</span></span>
- <span data-ttu-id="9c002-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9c002-131">SilentlyContinue</span></span>
- <span data-ttu-id="9c002-132">Finaliza</span><span class="sxs-lookup"><span data-stu-id="9c002-132">Stop</span></span>
- <span data-ttu-id="9c002-133">Suspensão</span><span class="sxs-lookup"><span data-stu-id="9c002-133">Suspend</span></span>

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

### <span data-ttu-id="9c002-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9c002-134">-InformationVariable</span></span>
<span data-ttu-id="9c002-135">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="9c002-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9c002-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="9c002-136">-LockId</span></span>
<span data-ttu-id="9c002-137">Especifica a ID do bloqueio.</span><span class="sxs-lookup"><span data-stu-id="9c002-137">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="9c002-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="9c002-138">-LockLevel</span></span>
<span data-ttu-id="9c002-139">Especifica o nível para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="9c002-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="9c002-140">Atualmente, os valores válidos são CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="9c002-140">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="9c002-141">-Lockname</span><span class="sxs-lookup"><span data-stu-id="9c002-141">-LockName</span></span>
<span data-ttu-id="9c002-142">Especifica o nome do bloqueio.</span><span class="sxs-lookup"><span data-stu-id="9c002-142">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="9c002-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="9c002-143">-LockNotes</span></span>
<span data-ttu-id="9c002-144">Especifica as anotações para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="9c002-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="9c002-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="9c002-145">-Pre</span></span>
<span data-ttu-id="9c002-146">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="9c002-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9c002-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c002-147">-ResourceGroupName</span></span>
<span data-ttu-id="9c002-148">Especifica o nome de um grupo de recursos para o qual o bloqueio se aplica ou que contém o grupo de recursos ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="9c002-148">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="9c002-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9c002-149">-ResourceName</span></span>
<span data-ttu-id="9c002-150">Especifica o nome do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="9c002-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="9c002-151">Por exemplo, para especificar um banco de dados, use o seguinte formato: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="9c002-151">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="9c002-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9c002-152">-ResourceType</span></span>
<span data-ttu-id="9c002-153">Especifica o tipo de recurso do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="9c002-153">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="9c002-154">-Escopo</span><span class="sxs-lookup"><span data-stu-id="9c002-154">-Scope</span></span>
<span data-ttu-id="9c002-155">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="9c002-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="9c002-156">Por exemplo, para especificar um banco de dados, use o seguinte formato: nome `/subscriptions/` do grupo de recursos de ID de assinatura nome `/resourceGroups/` do nome `/providers/Microsoft.Sql/servers/` do grupo de recursos `/databases/` para especificar um grupo de recursos, use o seguinte formato: `/subscriptions/` nome do grupo de recursos de ID de assinatura `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="9c002-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="9c002-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="9c002-157">-TenantLevel</span></span>
<span data-ttu-id="9c002-158">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="9c002-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="9c002-159">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9c002-159">-Confirm</span></span>
<span data-ttu-id="9c002-160">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c002-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c002-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c002-161">-WhatIf</span></span>
<span data-ttu-id="9c002-162">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c002-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c002-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c002-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c002-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c002-164">CommonParameters</span></span>
<span data-ttu-id="9c002-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c002-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c002-166">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c002-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c002-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c002-167">INPUTS</span></span>

## <span data-ttu-id="9c002-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c002-168">OUTPUTS</span></span>

## <span data-ttu-id="9c002-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c002-169">NOTES</span></span>

## <span data-ttu-id="9c002-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c002-170">RELATED LINKS</span></span>

[<span data-ttu-id="9c002-171">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="9c002-171">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="9c002-172">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="9c002-172">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="9c002-173">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="9c002-173">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


