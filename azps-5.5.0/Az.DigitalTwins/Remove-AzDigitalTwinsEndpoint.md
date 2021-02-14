---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 1c740134cb2613a8efcd950fec4cd780f4f443cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115808"
---
# <span data-ttu-id="2c0e4-101">Remove-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c0e4-101">Remove-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="2c0e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c0e4-102">SYNOPSIS</span></span>
<span data-ttu-id="2c0e4-103">Exclua um ponto de extremidade DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-103">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="2c0e4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c0e4-104">SYNTAX</span></span>

### <span data-ttu-id="2c0e4-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2c0e4-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2c0e4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2c0e4-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2c0e4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c0e4-107">DESCRIPTION</span></span>
<span data-ttu-id="2c0e4-108">Exclua um ponto de extremidade DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-108">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="2c0e4-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2c0e4-109">EXAMPLES</span></span>

### <span data-ttu-id="2c0e4-110">Exemplo 1: Excluir o azDigitalTwinsEndPoint pelo EndPointName</span><span class="sxs-lookup"><span data-stu-id="2c0e4-110">Example 1: Delete the azDigitalTwinsEndPoint by EndPointName</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -EndpointName youriEHEndpoint -ResourceName youriDigitalTwinsTest

```

<span data-ttu-id="2c0e4-111">Excluir o azDigitalTwinsEndPoint por EndPointName ResourceGroupName e ResourceName</span><span class="sxs-lookup"><span data-stu-id="2c0e4-111">Delete the azDigitalTwinsEndPoint by EndPointName ResourceGroupName and ResourceName</span></span>

### <span data-ttu-id="2c0e4-112">Exemplo 2: Excluir o azDigitalTwinsEndPoint por Objeto</span><span class="sxs-lookup"><span data-stu-id="2c0e4-112">Example 2: Delete the azDigitalTwinsEndPoint by Object</span></span>
```powershell
PS C:\> $GetAzdigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriEHEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsEndpoint -InputObject $GetAzdigitalTwinsEndpoint

```

<span data-ttu-id="2c0e4-113">Excluir o azDigitalTwinsEndPoint por Objeto</span><span class="sxs-lookup"><span data-stu-id="2c0e4-113">Delete the azDigitalTwinsEndPoint by Object</span></span>

## <span data-ttu-id="2c0e4-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c0e4-114">PARAMETERS</span></span>

### <span data-ttu-id="2c0e4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c0e4-115">-AsJob</span></span>
<span data-ttu-id="2c0e4-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="2c0e4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2c0e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c0e4-117">-DefaultProfile</span></span>
<span data-ttu-id="2c0e4-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c0e4-119">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="2c0e4-119">-EndpointName</span></span>
<span data-ttu-id="2c0e4-120">Nome do Recurso do Ponto de Extremidade.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-120">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="2c0e4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c0e4-121">-InputObject</span></span>
<span data-ttu-id="2c0e4-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2c0e4-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2c0e4-123">-NoWait</span></span>
<span data-ttu-id="2c0e4-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="2c0e4-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2c0e4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c0e4-125">-PassThru</span></span>
<span data-ttu-id="2c0e4-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="2c0e4-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2c0e4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c0e4-127">-ResourceGroupName</span></span>
<span data-ttu-id="2c0e4-128">O nome do grupo de recursos que contém a DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-128">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="2c0e4-129">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2c0e4-129">-ResourceName</span></span>
<span data-ttu-id="2c0e4-130">O nome da DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-130">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="2c0e4-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c0e4-131">-SubscriptionId</span></span>
<span data-ttu-id="2c0e4-132">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-132">The subscription identifier.</span></span>

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

### <span data-ttu-id="2c0e4-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2c0e4-133">-Confirm</span></span>
<span data-ttu-id="2c0e4-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c0e4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c0e4-135">-WhatIf</span></span>
<span data-ttu-id="2c0e4-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c0e4-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c0e4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c0e4-138">CommonParameters</span></span>
<span data-ttu-id="2c0e4-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c0e4-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c0e4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c0e4-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="2c0e4-141">INPUTS</span></span>

### <span data-ttu-id="2c0e4-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="2c0e4-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="2c0e4-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="2c0e4-143">OUTPUTS</span></span>

### <span data-ttu-id="2c0e4-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="2c0e4-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="2c0e4-145">Notas</span><span class="sxs-lookup"><span data-stu-id="2c0e4-145">NOTES</span></span>

<span data-ttu-id="2c0e4-146">Aliases</span><span class="sxs-lookup"><span data-stu-id="2c0e4-146">ALIASES</span></span>

<span data-ttu-id="2c0e4-147">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="2c0e4-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2c0e4-148">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2c0e4-149">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2c0e4-150">INPUTOBJECT: <IDigitalTwinsIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="2c0e4-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2c0e4-151">`[EndpointName <String>]`: Nome do Recurso do Ponto de Extremidade.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="2c0e4-152">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="2c0e4-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2c0e4-153">`[Location <String>]`: Localização do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="2c0e4-154">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="2c0e4-155">`[ResourceName <String>]`: o nome da DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="2c0e4-156">`[SubscriptionId <String>]`: o identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="2c0e4-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="2c0e4-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c0e4-157">RELATED LINKS</span></span>

