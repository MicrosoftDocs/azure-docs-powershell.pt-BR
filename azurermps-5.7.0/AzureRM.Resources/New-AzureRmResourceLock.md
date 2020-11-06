---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
ms.openlocfilehash: 0b3498ba3107e2312b596143820036286b925b6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602360"
---
# <span data-ttu-id="a664b-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a664b-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="a664b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a664b-102">SYNOPSIS</span></span>
<span data-ttu-id="a664b-103">Cria um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="a664b-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a664b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a664b-104">SYNTAX</span></span>

### <span data-ttu-id="a664b-105">BySpecifiedScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="a664b-105">BySpecifiedScope (Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a664b-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a664b-106">ByResourceGroup</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a664b-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="a664b-107">ByResourceGroupLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a664b-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="a664b-108">BySubscription</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a664b-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="a664b-109">BySubscriptionLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a664b-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="a664b-110">ByTenantLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a664b-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="a664b-111">ByLockId</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a664b-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a664b-112">DESCRIPTION</span></span>
<span data-ttu-id="a664b-113">O cmdlet **New-AzureRmResourceLock** cria um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="a664b-113">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="a664b-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a664b-114">EXAMPLES</span></span>

### <span data-ttu-id="a664b-115">Exemplo 1: criar um bloqueio de recurso em um site</span><span class="sxs-lookup"><span data-stu-id="a664b-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="a664b-116">Esse comando cria um bloqueio de recurso em um site.</span><span class="sxs-lookup"><span data-stu-id="a664b-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="a664b-117">OS</span><span class="sxs-lookup"><span data-stu-id="a664b-117">PARAMETERS</span></span>

### <span data-ttu-id="a664b-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a664b-118">-ApiVersion</span></span>
<span data-ttu-id="a664b-119">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="a664b-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a664b-120">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="a664b-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a664b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a664b-121">-DefaultProfile</span></span>
<span data-ttu-id="a664b-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a664b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a664b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a664b-123">-Force</span></span>
<span data-ttu-id="a664b-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a664b-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a664b-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="a664b-125">-InformationAction</span></span>
<span data-ttu-id="a664b-126">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="a664b-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a664b-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a664b-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a664b-128">Contínuo</span><span class="sxs-lookup"><span data-stu-id="a664b-128">Continue</span></span>
- <span data-ttu-id="a664b-129">Ignorar</span><span class="sxs-lookup"><span data-stu-id="a664b-129">Ignore</span></span>
- <span data-ttu-id="a664b-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="a664b-130">Inquire</span></span>
- <span data-ttu-id="a664b-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a664b-131">SilentlyContinue</span></span>
- <span data-ttu-id="a664b-132">Finaliza</span><span class="sxs-lookup"><span data-stu-id="a664b-132">Stop</span></span>
- <span data-ttu-id="a664b-133">Suspensão</span><span class="sxs-lookup"><span data-stu-id="a664b-133">Suspend</span></span>

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

### <span data-ttu-id="a664b-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a664b-134">-InformationVariable</span></span>
<span data-ttu-id="a664b-135">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="a664b-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a664b-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="a664b-136">-LockId</span></span>
<span data-ttu-id="a664b-137">Especifica a ID do bloqueio.</span><span class="sxs-lookup"><span data-stu-id="a664b-137">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="a664b-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="a664b-138">-LockLevel</span></span>
<span data-ttu-id="a664b-139">Especifica o nível para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="a664b-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="a664b-140">Atualmente, os valores válidos são CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="a664b-140">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="a664b-141">-Lockname</span><span class="sxs-lookup"><span data-stu-id="a664b-141">-LockName</span></span>
<span data-ttu-id="a664b-142">Especifica o nome do bloqueio.</span><span class="sxs-lookup"><span data-stu-id="a664b-142">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="a664b-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="a664b-143">-LockNotes</span></span>
<span data-ttu-id="a664b-144">Especifica as anotações para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="a664b-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="a664b-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="a664b-145">-Pre</span></span>
<span data-ttu-id="a664b-146">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="a664b-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a664b-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a664b-147">-ResourceGroupName</span></span>
<span data-ttu-id="a664b-148">Especifica o nome de um grupo de recursos para o qual o bloqueio se aplica ou que contém o grupo de recursos ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="a664b-148">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="a664b-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a664b-149">-ResourceName</span></span>
<span data-ttu-id="a664b-150">Especifica o nome do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="a664b-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="a664b-151">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="a664b-151">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

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

### <span data-ttu-id="a664b-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a664b-152">-ResourceType</span></span>
<span data-ttu-id="a664b-153">Especifica o tipo de recurso do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="a664b-153">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="a664b-154">-Escopo</span><span class="sxs-lookup"><span data-stu-id="a664b-154">-Scope</span></span>
<span data-ttu-id="a664b-155">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="a664b-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="a664b-156">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="a664b-156">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="a664b-157">`/subscriptions/`ID `/resourceGroups/` do grupo de recursos nome do grupo nome `/providers/Microsoft.Sql/servers/` do `/databases/` banco de dados</span><span class="sxs-lookup"><span data-stu-id="a664b-157">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="a664b-158">Para especificar um grupo de recursos, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="a664b-158">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="a664b-159">`/subscriptions/`ID da assinatura `/resourceGroups/` nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a664b-159">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="a664b-160">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="a664b-160">-TenantLevel</span></span>
<span data-ttu-id="a664b-161">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="a664b-161">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="a664b-162">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a664b-162">-Confirm</span></span>
<span data-ttu-id="a664b-163">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a664b-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a664b-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a664b-164">-WhatIf</span></span>
<span data-ttu-id="a664b-165">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a664b-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a664b-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a664b-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a664b-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a664b-167">CommonParameters</span></span>
<span data-ttu-id="a664b-168">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a664b-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a664b-169">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a664b-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a664b-170">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a664b-170">INPUTS</span></span>

### <span data-ttu-id="a664b-171">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a664b-171">None</span></span>
<span data-ttu-id="a664b-172">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a664b-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a664b-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a664b-173">OUTPUTS</span></span>

### <span data-ttu-id="a664b-174">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a664b-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a664b-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a664b-175">NOTES</span></span>

## <span data-ttu-id="a664b-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a664b-176">RELATED LINKS</span></span>

[<span data-ttu-id="a664b-177">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a664b-177">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="a664b-178">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a664b-178">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="a664b-179">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a664b-179">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


