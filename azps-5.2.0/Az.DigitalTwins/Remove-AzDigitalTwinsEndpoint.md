---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 1c740134cb2613a8efcd950fec4cd780f4f443cf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260543"
---
# <span data-ttu-id="6b06e-101">Remove-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="6b06e-101">Remove-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="6b06e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b06e-102">SYNOPSIS</span></span>
<span data-ttu-id="6b06e-103">Exclua um ponto de extremidade do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="6b06e-103">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="6b06e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b06e-104">SYNTAX</span></span>

### <span data-ttu-id="6b06e-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="6b06e-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6b06e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6b06e-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6b06e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b06e-107">DESCRIPTION</span></span>
<span data-ttu-id="6b06e-108">Exclua um ponto de extremidade do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="6b06e-108">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="6b06e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b06e-109">EXAMPLES</span></span>

### <span data-ttu-id="6b06e-110">Exemplo 1: excluir o azDigitalTwinsEndPoint por EndpointName</span><span class="sxs-lookup"><span data-stu-id="6b06e-110">Example 1: Delete the azDigitalTwinsEndPoint by EndPointName</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -EndpointName youriEHEndpoint -ResourceName youriDigitalTwinsTest

```

<span data-ttu-id="6b06e-111">Excluir o azDigitalTwinsEndPoint de EndpointName ResourceGroupName e resourceName</span><span class="sxs-lookup"><span data-stu-id="6b06e-111">Delete the azDigitalTwinsEndPoint by EndPointName ResourceGroupName and ResourceName</span></span>

### <span data-ttu-id="6b06e-112">Exemplo 2: excluir o azDigitalTwinsEndPoint por objeto</span><span class="sxs-lookup"><span data-stu-id="6b06e-112">Example 2: Delete the azDigitalTwinsEndPoint by Object</span></span>
```powershell
PS C:\> $GetAzdigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriEHEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsEndpoint -InputObject $GetAzdigitalTwinsEndpoint

```

<span data-ttu-id="6b06e-113">Excluir o azDigitalTwinsEndPoint por objeto</span><span class="sxs-lookup"><span data-stu-id="6b06e-113">Delete the azDigitalTwinsEndPoint by Object</span></span>

## <span data-ttu-id="6b06e-114">OS</span><span class="sxs-lookup"><span data-stu-id="6b06e-114">PARAMETERS</span></span>

### <span data-ttu-id="6b06e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b06e-115">-AsJob</span></span>
<span data-ttu-id="6b06e-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="6b06e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6b06e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b06e-117">-DefaultProfile</span></span>
<span data-ttu-id="6b06e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b06e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b06e-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6b06e-119">-EndpointName</span></span>
<span data-ttu-id="6b06e-120">Nome do recurso de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="6b06e-120">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="6b06e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b06e-121">-InputObject</span></span>
<span data-ttu-id="6b06e-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6b06e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b06e-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6b06e-123">-NoWait</span></span>
<span data-ttu-id="6b06e-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="6b06e-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6b06e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b06e-125">-PassThru</span></span>
<span data-ttu-id="6b06e-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="6b06e-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6b06e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b06e-127">-ResourceGroupName</span></span>
<span data-ttu-id="6b06e-128">O nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="6b06e-128">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="6b06e-129">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6b06e-129">-ResourceName</span></span>
<span data-ttu-id="6b06e-130">O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="6b06e-130">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="6b06e-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b06e-131">-SubscriptionId</span></span>
<span data-ttu-id="6b06e-132">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="6b06e-132">The subscription identifier.</span></span>

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

### <span data-ttu-id="6b06e-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6b06e-133">-Confirm</span></span>
<span data-ttu-id="6b06e-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b06e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b06e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b06e-135">-WhatIf</span></span>
<span data-ttu-id="6b06e-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6b06e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b06e-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b06e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b06e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b06e-138">CommonParameters</span></span>
<span data-ttu-id="6b06e-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b06e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b06e-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b06e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b06e-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b06e-141">INPUTS</span></span>

### <span data-ttu-id="6b06e-142">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="6b06e-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="6b06e-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b06e-143">OUTPUTS</span></span>

### <span data-ttu-id="6b06e-144">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. Api20201031. IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="6b06e-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="6b06e-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b06e-145">NOTES</span></span>

<span data-ttu-id="6b06e-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6b06e-146">ALIASES</span></span>

<span data-ttu-id="6b06e-147">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="6b06e-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b06e-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="6b06e-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b06e-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6b06e-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b06e-150">INPUTobject <IDigitalTwinsIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="6b06e-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6b06e-151">`[EndpointName <String>]`: Nome do recurso de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="6b06e-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="6b06e-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="6b06e-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6b06e-153">`[Location <String>]`: Local do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="6b06e-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="6b06e-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="6b06e-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="6b06e-155">`[ResourceName <String>]`: O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="6b06e-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="6b06e-156">`[SubscriptionId <String>]`: O identificador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="6b06e-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="6b06e-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b06e-157">RELATED LINKS</span></span>

