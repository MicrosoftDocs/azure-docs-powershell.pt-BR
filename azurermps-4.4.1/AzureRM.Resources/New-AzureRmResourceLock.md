---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
ms.openlocfilehash: c363279c0cbb6dc20b0ddcc7bae32266a848fb3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440957"
---
# <span data-ttu-id="44c45-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="44c45-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="44c45-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44c45-102">SYNOPSIS</span></span>
<span data-ttu-id="44c45-103">Cria um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="44c45-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44c45-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44c45-104">SYNTAX</span></span>

### <span data-ttu-id="44c45-105">Um bloqueio no escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="44c45-105">A lock at the specified scope.</span></span> <span data-ttu-id="44c45-106">Assume</span><span class="sxs-lookup"><span data-stu-id="44c45-106">(Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44c45-107">Um bloqueio no escopo do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44c45-107">A lock at the resource group scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44c45-108">Um bloqueio no escopo de recursos do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44c45-108">A lock at the resource group resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44c45-109">Um bloqueio no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="44c45-109">A lock at the subscription scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44c45-110">Um bloqueio no escopo do recurso de assinatura.</span><span class="sxs-lookup"><span data-stu-id="44c45-110">A lock at the subscription resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44c45-111">Um bloqueio no escopo do recurso locatário.</span><span class="sxs-lookup"><span data-stu-id="44c45-111">A lock at the tenant resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44c45-112">Um lock, por ID.</span><span class="sxs-lookup"><span data-stu-id="44c45-112">A lock, by Id.</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44c45-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44c45-113">DESCRIPTION</span></span>
<span data-ttu-id="44c45-114">O cmdlet **New-AzureRmResourceLock** cria um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="44c45-114">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="44c45-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44c45-115">EXAMPLES</span></span>

### <span data-ttu-id="44c45-116">Exemplo 1: criar um bloqueio de recurso em um site</span><span class="sxs-lookup"><span data-stu-id="44c45-116">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="44c45-117">Esse comando cria um bloqueio de recurso em um site.</span><span class="sxs-lookup"><span data-stu-id="44c45-117">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="44c45-118">OS</span><span class="sxs-lookup"><span data-stu-id="44c45-118">PARAMETERS</span></span>

### <span data-ttu-id="44c45-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="44c45-119">-ApiVersion</span></span>
<span data-ttu-id="44c45-120">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="44c45-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="44c45-121">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="44c45-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="44c45-122">-Force</span><span class="sxs-lookup"><span data-stu-id="44c45-122">-Force</span></span>
<span data-ttu-id="44c45-123">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="44c45-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="44c45-124">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="44c45-124">-InformationAction</span></span>
<span data-ttu-id="44c45-125">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="44c45-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="44c45-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="44c45-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="44c45-127">Contínuo</span><span class="sxs-lookup"><span data-stu-id="44c45-127">Continue</span></span>
- <span data-ttu-id="44c45-128">Ignorar</span><span class="sxs-lookup"><span data-stu-id="44c45-128">Ignore</span></span>
- <span data-ttu-id="44c45-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="44c45-129">Inquire</span></span>
- <span data-ttu-id="44c45-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="44c45-130">SilentlyContinue</span></span>
- <span data-ttu-id="44c45-131">Finaliza</span><span class="sxs-lookup"><span data-stu-id="44c45-131">Stop</span></span>
- <span data-ttu-id="44c45-132">Suspensão</span><span class="sxs-lookup"><span data-stu-id="44c45-132">Suspend</span></span>

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

### <span data-ttu-id="44c45-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="44c45-133">-InformationVariable</span></span>
<span data-ttu-id="44c45-134">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="44c45-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="44c45-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="44c45-135">-LockId</span></span>
<span data-ttu-id="44c45-136">Especifica a ID do bloqueio.</span><span class="sxs-lookup"><span data-stu-id="44c45-136">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="44c45-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="44c45-137">-LockLevel</span></span>
<span data-ttu-id="44c45-138">Especifica o nível para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="44c45-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="44c45-139">Atualmente, o único valor válido é CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="44c45-139">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="44c45-140">-Lockname</span><span class="sxs-lookup"><span data-stu-id="44c45-140">-LockName</span></span>
<span data-ttu-id="44c45-141">Especifica o nome do bloqueio.</span><span class="sxs-lookup"><span data-stu-id="44c45-141">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="44c45-142">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="44c45-142">-LockNotes</span></span>
<span data-ttu-id="44c45-143">Especifica as anotações para o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="44c45-143">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="44c45-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="44c45-144">-Pre</span></span>
<span data-ttu-id="44c45-145">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="44c45-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="44c45-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44c45-146">-ResourceGroupName</span></span>
<span data-ttu-id="44c45-147">Especifica o nome de um grupo de recursos para o qual o bloqueio se aplica ou que contém o grupo de recursos ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="44c45-147">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="44c45-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="44c45-148">-ResourceName</span></span>
<span data-ttu-id="44c45-149">Especifica o nome do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="44c45-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="44c45-150">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="44c45-150">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

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

### <span data-ttu-id="44c45-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="44c45-151">-ResourceType</span></span>
<span data-ttu-id="44c45-152">Especifica o tipo de recurso do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="44c45-152">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="44c45-153">-Escopo</span><span class="sxs-lookup"><span data-stu-id="44c45-153">-Scope</span></span>
<span data-ttu-id="44c45-154">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="44c45-154">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="44c45-155">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="44c45-155">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="44c45-156">`/subscriptions/`ID `/resourceGroups/` do grupo de recursos nome do grupo nome `/providers/Microsoft.Sql/servers/` do `/databases/` banco de dados</span><span class="sxs-lookup"><span data-stu-id="44c45-156">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="44c45-157">Para especificar um grupo de recursos, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="44c45-157">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="44c45-158">`/subscriptions/`ID da assinatura `/resourceGroups/` nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="44c45-158">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="44c45-159">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="44c45-159">-TenantLevel</span></span>
<span data-ttu-id="44c45-160">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="44c45-160">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="44c45-161">-Confirme</span><span class="sxs-lookup"><span data-stu-id="44c45-161">-Confirm</span></span>
<span data-ttu-id="44c45-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44c45-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44c45-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44c45-163">-WhatIf</span></span>
<span data-ttu-id="44c45-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44c45-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44c45-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44c45-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44c45-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c45-166">-DefaultProfile</span></span>
<span data-ttu-id="44c45-167">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44c45-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44c45-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c45-168">CommonParameters</span></span>
<span data-ttu-id="44c45-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44c45-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c45-170">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44c45-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c45-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44c45-171">INPUTS</span></span>

## <span data-ttu-id="44c45-172">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44c45-172">OUTPUTS</span></span>

### <span data-ttu-id="44c45-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="44c45-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="44c45-174">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44c45-174">NOTES</span></span>

## <span data-ttu-id="44c45-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44c45-175">RELATED LINKS</span></span>

[<span data-ttu-id="44c45-176">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="44c45-176">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="44c45-177">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="44c45-177">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="44c45-178">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="44c45-178">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


