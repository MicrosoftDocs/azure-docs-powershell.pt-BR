---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/remove-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Remove-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Remove-AzConfluentOrganization.md
ms.openlocfilehash: d35de003bd4822758fd75c7dbbcf616ebecbbccb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893221"
---
# <span data-ttu-id="7d9f0-101">Remove-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="7d9f0-101">Remove-AzConfluentOrganization</span></span>

## <span data-ttu-id="7d9f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d9f0-102">SYNOPSIS</span></span>
<span data-ttu-id="7d9f0-103">Excluir recurso Organization</span><span class="sxs-lookup"><span data-stu-id="7d9f0-103">Delete Organization resource</span></span>

## <span data-ttu-id="7d9f0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7d9f0-104">SYNTAX</span></span>

### <span data-ttu-id="7d9f0-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7d9f0-105">Delete (Default)</span></span>
```
Remove-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7d9f0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7d9f0-106">DeleteViaIdentity</span></span>
```
Remove-AzConfluentOrganization -InputObject <IConfluentIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7d9f0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7d9f0-107">DESCRIPTION</span></span>
<span data-ttu-id="7d9f0-108">Excluir recurso Organization</span><span class="sxs-lookup"><span data-stu-id="7d9f0-108">Delete Organization resource</span></span>

## <span data-ttu-id="7d9f0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d9f0-109">EXAMPLES</span></span>

### <span data-ttu-id="7d9f0-110">Exemplo 1: Remover uma organização confluente pelo nome</span><span class="sxs-lookup"><span data-stu-id="7d9f0-110">Example 1: Remove a confluent organization by name</span></span>
```powershell
PS C:\> Remove-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-01-portal

```

<span data-ttu-id="7d9f0-111">Este comando remove uma organização confluente pelo nome</span><span class="sxs-lookup"><span data-stu-id="7d9f0-111">This command removes a confluent organization by name</span></span>

### <span data-ttu-id="7d9f0-112">Exemplo 2: Remover uma organização confluente por pipeline</span><span class="sxs-lookup"><span data-stu-id="7d9f0-112">Example 2: Remove a confluent organization by pipeline</span></span>
```powershell
PS C:\>  Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh | Remove-AzConfluentOrganization

```

<span data-ttu-id="7d9f0-113">Este comando remove uma organização confluente por pipeline.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-113">This command removes a confluent organization by pipeline.</span></span>

## <span data-ttu-id="7d9f0-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7d9f0-114">PARAMETERS</span></span>

### <span data-ttu-id="7d9f0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d9f0-115">-AsJob</span></span>
<span data-ttu-id="7d9f0-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="7d9f0-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7d9f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d9f0-117">-DefaultProfile</span></span>
<span data-ttu-id="7d9f0-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d9f0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d9f0-119">-InputObject</span></span>
<span data-ttu-id="7d9f0-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d9f0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7d9f0-121">-Name</span></span>
<span data-ttu-id="7d9f0-122">Nome do recurso da organização</span><span class="sxs-lookup"><span data-stu-id="7d9f0-122">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d9f0-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7d9f0-123">-NoWait</span></span>
<span data-ttu-id="7d9f0-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="7d9f0-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7d9f0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d9f0-125">-PassThru</span></span>
<span data-ttu-id="7d9f0-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="7d9f0-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7d9f0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d9f0-127">-ResourceGroupName</span></span>
<span data-ttu-id="7d9f0-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7d9f0-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d9f0-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d9f0-129">-SubscriptionId</span></span>
<span data-ttu-id="7d9f0-130">ID de assinatura do Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="7d9f0-130">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d9f0-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d9f0-131">-Confirm</span></span>
<span data-ttu-id="7d9f0-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d9f0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d9f0-133">-WhatIf</span></span>
<span data-ttu-id="7d9f0-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d9f0-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d9f0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d9f0-136">CommonParameters</span></span>
<span data-ttu-id="7d9f0-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d9f0-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d9f0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d9f0-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d9f0-139">INPUTS</span></span>

### <span data-ttu-id="7d9f0-140">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="7d9f0-140">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="7d9f0-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7d9f0-141">OUTPUTS</span></span>

### <span data-ttu-id="7d9f0-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7d9f0-142">System.Boolean</span></span>

## <span data-ttu-id="7d9f0-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="7d9f0-143">NOTES</span></span>

<span data-ttu-id="7d9f0-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7d9f0-144">ALIASES</span></span>

<span data-ttu-id="7d9f0-145">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="7d9f0-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7d9f0-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7d9f0-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7d9f0-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7d9f0-148">INPUTOBJECT <IConfluentIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="7d9f0-148">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7d9f0-149">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="7d9f0-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7d9f0-150">`[OrganizationName <String>]`: Nome do recurso da organização</span><span class="sxs-lookup"><span data-stu-id="7d9f0-150">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="7d9f0-151">`[ResourceGroupName <String>]`: Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7d9f0-151">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="7d9f0-152">`[SubscriptionId <String>]`: ID de assinatura do Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="7d9f0-152">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="7d9f0-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d9f0-153">RELATED LINKS</span></span>

