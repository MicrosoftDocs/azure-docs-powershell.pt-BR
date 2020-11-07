---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/remove-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: fe7c391b8f15e3389a9d61070b8f55d47af6d6ec
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775983"
---
# <span data-ttu-id="f0916-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="f0916-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="f0916-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0916-102">SYNOPSIS</span></span>
<span data-ttu-id="f0916-103">Excluir uma cota por nome.</span><span class="sxs-lookup"><span data-stu-id="f0916-103">Delete a quota by name.</span></span>

## <span data-ttu-id="f0916-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0916-104">SYNTAX</span></span>

### <span data-ttu-id="f0916-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="f0916-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f0916-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f0916-106">DeleteViaIdentity</span></span>
```
Remove-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f0916-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f0916-107">DESCRIPTION</span></span>
<span data-ttu-id="f0916-108">Excluir uma cota por nome.</span><span class="sxs-lookup"><span data-stu-id="f0916-108">Delete a quota by name.</span></span>

## <span data-ttu-id="f0916-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0916-109">EXAMPLES</span></span>

### <span data-ttu-id="f0916-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f0916-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="f0916-111">Remova uma cota de rede por nome.</span><span class="sxs-lookup"><span data-stu-id="f0916-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="f0916-112">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="f0916-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="f0916-113">Remova uma cota de rede usando um pipe.</span><span class="sxs-lookup"><span data-stu-id="f0916-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="f0916-114">--------------------------EXEMPLO 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="f0916-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="f0916-115">Remover uma cota de rede.</span><span class="sxs-lookup"><span data-stu-id="f0916-115">Remove a network quota.</span></span>

## <span data-ttu-id="f0916-116">OS</span><span class="sxs-lookup"><span data-stu-id="f0916-116">PARAMETERS</span></span>

### <span data-ttu-id="f0916-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0916-117">-AsJob</span></span>
<span data-ttu-id="f0916-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="f0916-118">Run the command as a job</span></span>

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

### <span data-ttu-id="f0916-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0916-119">-DefaultProfile</span></span>
<span data-ttu-id="f0916-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f0916-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0916-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0916-121">-InputObject</span></span>
<span data-ttu-id="f0916-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f0916-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f0916-123">-Local</span><span class="sxs-lookup"><span data-stu-id="f0916-123">-Location</span></span>
<span data-ttu-id="f0916-124">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="f0916-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f0916-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0916-125">-Name</span></span>
<span data-ttu-id="f0916-126">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="f0916-126">Name of the resource.</span></span>

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

### <span data-ttu-id="f0916-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f0916-127">-NoWait</span></span>
<span data-ttu-id="f0916-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="f0916-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f0916-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0916-129">-PassThru</span></span>
<span data-ttu-id="f0916-130">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="f0916-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f0916-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f0916-131">-SubscriptionId</span></span>
<span data-ttu-id="f0916-132">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f0916-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f0916-133">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f0916-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f0916-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f0916-134">-Confirm</span></span>
<span data-ttu-id="f0916-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0916-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0916-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0916-136">-WhatIf</span></span>
<span data-ttu-id="f0916-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f0916-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0916-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f0916-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0916-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0916-139">CommonParameters</span></span>
<span data-ttu-id="f0916-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0916-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0916-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0916-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0916-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f0916-142">INPUTS</span></span>

### <span data-ttu-id="f0916-143">Microsoft. Azure. PowerShell. cmdlets. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="f0916-143">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="f0916-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f0916-144">OUTPUTS</span></span>

### <span data-ttu-id="f0916-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f0916-145">System.Boolean</span></span>



## <span data-ttu-id="f0916-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f0916-146">NOTES</span></span>

<span data-ttu-id="f0916-147">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="f0916-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f0916-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f0916-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f0916-149">INPUTobject <INetworkAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="f0916-149">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f0916-150">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="f0916-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f0916-151">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="f0916-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="f0916-152">`[ResourceName <String>]`: Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="f0916-152">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="f0916-153">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f0916-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f0916-154">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f0916-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f0916-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0916-155">RELATED LINKS</span></span>
