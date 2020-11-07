---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/resume-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: 65d2b3a045d38435cdd709d47c0be88f7fc98af0
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945249"
---
# <span data-ttu-id="71f8f-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="71f8f-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="71f8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="71f8f-103">Retomar uma atualização com falha.</span><span class="sxs-lookup"><span data-stu-id="71f8f-103">Resume a failed update.</span></span>

## <span data-ttu-id="71f8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71f8f-104">SYNTAX</span></span>

### <span data-ttu-id="71f8f-105">Executar novamente (padrão)</span><span class="sxs-lookup"><span data-stu-id="71f8f-105">Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="71f8f-106">RerunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="71f8f-106">RerunViaIdentity</span></span>
```
Resume-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="71f8f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71f8f-107">DESCRIPTION</span></span>
<span data-ttu-id="71f8f-108">Retomar uma atualização com falha.</span><span class="sxs-lookup"><span data-stu-id="71f8f-108">Resume a failed update.</span></span>

## <span data-ttu-id="71f8f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71f8f-109">EXAMPLES</span></span>

### <span data-ttu-id="71f8f-110">Exemplo 1: Resume-AzsUpdateRun por nome e updatename</span><span class="sxs-lookup"><span data-stu-id="71f8f-110">Example 1: Resume-AzsUpdateRun By Name and UpdateName</span></span>
```powershell
PS C:\> Resume-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4

```

<span data-ttu-id="71f8f-111">O commandlet permite executar novamente uma execução de atualização específica com falha.</span><span class="sxs-lookup"><span data-stu-id="71f8f-111">Commandlet allows you to rerun a specific failed update run.</span></span>
<span data-ttu-id="71f8f-112">Observe que há um requisito de que a versão de atualização seja estritamente maior do que a versão atual.</span><span class="sxs-lookup"><span data-stu-id="71f8f-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="71f8f-113">OS</span><span class="sxs-lookup"><span data-stu-id="71f8f-113">PARAMETERS</span></span>

### <span data-ttu-id="71f8f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71f8f-114">-DefaultProfile</span></span>
<span data-ttu-id="71f8f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71f8f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71f8f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71f8f-116">-InputObject</span></span>
<span data-ttu-id="71f8f-117">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="71f8f-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: RerunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="71f8f-118">-Local</span><span class="sxs-lookup"><span data-stu-id="71f8f-118">-Location</span></span>
<span data-ttu-id="71f8f-119">O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="71f8f-119">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="71f8f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="71f8f-120">-Name</span></span>
<span data-ttu-id="71f8f-121">Identificador de execução de atualização.</span><span class="sxs-lookup"><span data-stu-id="71f8f-121">Update run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="71f8f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71f8f-122">-PassThru</span></span>
<span data-ttu-id="71f8f-123">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="71f8f-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="71f8f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71f8f-124">-ResourceGroupName</span></span>
<span data-ttu-id="71f8f-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71f8f-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="71f8f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71f8f-126">-SubscriptionId</span></span>
<span data-ttu-id="71f8f-127">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="71f8f-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="71f8f-128">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="71f8f-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="71f8f-129">-Updatename</span><span class="sxs-lookup"><span data-stu-id="71f8f-129">-UpdateName</span></span>
<span data-ttu-id="71f8f-130">Nome da atualização.</span><span class="sxs-lookup"><span data-stu-id="71f8f-130">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="71f8f-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71f8f-131">-Confirm</span></span>
<span data-ttu-id="71f8f-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71f8f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71f8f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71f8f-133">-WhatIf</span></span>
<span data-ttu-id="71f8f-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71f8f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71f8f-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71f8f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71f8f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71f8f-136">CommonParameters</span></span>
<span data-ttu-id="71f8f-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71f8f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71f8f-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71f8f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71f8f-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71f8f-139">INPUTS</span></span>

### <span data-ttu-id="71f8f-140">Microsoft. Azure. PowerShell. cmdlets. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="71f8f-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="71f8f-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71f8f-141">OUTPUTS</span></span>

### <span data-ttu-id="71f8f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71f8f-142">System.Boolean</span></span>



## <span data-ttu-id="71f8f-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71f8f-143">NOTES</span></span>

<span data-ttu-id="71f8f-144">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="71f8f-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="71f8f-145">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="71f8f-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="71f8f-146">INPUTobject <IUpdateAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="71f8f-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="71f8f-147">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="71f8f-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="71f8f-148">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71f8f-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="71f8f-149">`[RunName <String>]`: Atualizar identificador de execução.</span><span class="sxs-lookup"><span data-stu-id="71f8f-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="71f8f-150">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="71f8f-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="71f8f-151">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="71f8f-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="71f8f-152">`[UpdateLocation <String>]`: O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="71f8f-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="71f8f-153">`[UpdateName <String>]`: Nome da atualização.</span><span class="sxs-lookup"><span data-stu-id="71f8f-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="71f8f-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71f8f-154">RELATED LINKS</span></span>

