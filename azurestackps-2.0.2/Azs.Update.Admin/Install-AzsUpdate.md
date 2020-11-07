---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/install-azsupdate
schema: 2.0.0
ms.openlocfilehash: e6fc8ee19443f0861fb867a5e60d0f637642ff62
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946924"
---
# <span data-ttu-id="5121c-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="5121c-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="5121c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5121c-102">SYNOPSIS</span></span>
<span data-ttu-id="5121c-103">Aplicar uma atualização específica em um local de atualização.</span><span class="sxs-lookup"><span data-stu-id="5121c-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="5121c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5121c-104">SYNTAX</span></span>

### <span data-ttu-id="5121c-105">Aplicar (padrão)</span><span class="sxs-lookup"><span data-stu-id="5121c-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5121c-106">ApplyViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5121c-106">ApplyViaIdentity</span></span>
```
Install-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5121c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5121c-107">DESCRIPTION</span></span>
<span data-ttu-id="5121c-108">Aplicar uma atualização específica em um local de atualização.</span><span class="sxs-lookup"><span data-stu-id="5121c-108">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="5121c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5121c-109">EXAMPLES</span></span>

### <span data-ttu-id="5121c-110">Exemplo 1: Install-AzsUpdate por nome</span><span class="sxs-lookup"><span data-stu-id="5121c-110">Example 1: Install-AzsUpdate By Name</span></span>
```powershell
PS C:\> Install-AzsUpdate -Name Microsoft1.1907.0.10
```

<span data-ttu-id="5121c-111">O commandlet permite que você instale atualizações específicas por nome.</span><span class="sxs-lookup"><span data-stu-id="5121c-111">Commandlet allows you to install specific updates by name.</span></span>
<span data-ttu-id="5121c-112">Observe que há um requisito de que a versão de atualização seja estritamente maior do que a versão atual.</span><span class="sxs-lookup"><span data-stu-id="5121c-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="5121c-113">OS</span><span class="sxs-lookup"><span data-stu-id="5121c-113">PARAMETERS</span></span>

### <span data-ttu-id="5121c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5121c-114">-AsJob</span></span>
<span data-ttu-id="5121c-115">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="5121c-115">Run the command as a job</span></span>

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

### <span data-ttu-id="5121c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5121c-116">-DefaultProfile</span></span>
<span data-ttu-id="5121c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5121c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5121c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5121c-118">-InputObject</span></span>
<span data-ttu-id="5121c-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5121c-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: ApplyViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5121c-120">-Local</span><span class="sxs-lookup"><span data-stu-id="5121c-120">-Location</span></span>
<span data-ttu-id="5121c-121">O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="5121c-121">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5121c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5121c-122">-Name</span></span>
<span data-ttu-id="5121c-123">Nome da atualização.</span><span class="sxs-lookup"><span data-stu-id="5121c-123">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5121c-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5121c-124">-NoWait</span></span>
<span data-ttu-id="5121c-125">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="5121c-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5121c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5121c-126">-ResourceGroupName</span></span>
<span data-ttu-id="5121c-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5121c-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5121c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5121c-128">-SubscriptionId</span></span>
<span data-ttu-id="5121c-129">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5121c-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5121c-130">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="5121c-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5121c-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5121c-131">-Confirm</span></span>
<span data-ttu-id="5121c-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5121c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5121c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5121c-133">-WhatIf</span></span>
<span data-ttu-id="5121c-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5121c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5121c-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5121c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5121c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5121c-136">CommonParameters</span></span>
<span data-ttu-id="5121c-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5121c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5121c-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5121c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5121c-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5121c-139">INPUTS</span></span>

### <span data-ttu-id="5121c-140">Microsoft. Azure. PowerShell. cmdlets. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5121c-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="5121c-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5121c-141">OUTPUTS</span></span>

### <span data-ttu-id="5121c-142">Microsoft. Azure. PowerShell. cmdlets. UpdateAdmin. Models. Api20160501. IUpdateRun</span><span class="sxs-lookup"><span data-stu-id="5121c-142">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="5121c-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5121c-143">NOTES</span></span>

<span data-ttu-id="5121c-144">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="5121c-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5121c-145">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5121c-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5121c-146">INPUTobject <IUpdateAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="5121c-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5121c-147">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="5121c-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5121c-148">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5121c-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="5121c-149">`[RunName <String>]`: Atualizar identificador de execução.</span><span class="sxs-lookup"><span data-stu-id="5121c-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="5121c-150">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5121c-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="5121c-151">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="5121c-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5121c-152">`[UpdateLocation <String>]`: O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="5121c-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="5121c-153">`[UpdateName <String>]`: Nome da atualização.</span><span class="sxs-lookup"><span data-stu-id="5121c-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="5121c-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5121c-154">RELATED LINKS</span></span>

