---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/remove-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
ms.openlocfilehash: ff83b10755789f807e1ec28b1f247c9ebee1da18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889511"
---
# <span data-ttu-id="ddc1d-101">Remove-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="ddc1d-101">Remove-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="ddc1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddc1d-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc1d-103">Exclua um DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ddc1d-103">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="ddc1d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ddc1d-104">SYNTAX</span></span>

### <span data-ttu-id="ddc1d-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ddc1d-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ddc1d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ddc1d-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ddc1d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ddc1d-107">DESCRIPTION</span></span>
<span data-ttu-id="ddc1d-108">Exclua um DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ddc1d-108">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="ddc1d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ddc1d-109">EXAMPLES</span></span>

### <span data-ttu-id="ddc1d-110">Exemplo 1: Remover um AzDigitalTwinsInstance pelo nome</span><span class="sxs-lookup"><span data-stu-id="ddc1d-110">Example 1: Remove an AzDigitalTwinsInstance by name</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin


```

<span data-ttu-id="ddc1d-111">Este comando remove um AzDigitalTwinsInstance pelo nome</span><span class="sxs-lookup"><span data-stu-id="ddc1d-111">This command removes an AzDigitalTwinsInstance by name</span></span>

### <span data-ttu-id="ddc1d-112">Exemplo 2: Remover um AzDigitalTwinsInstance por InputObject</span><span class="sxs-lookup"><span data-stu-id="ddc1d-112">Example 2: Remove an AzDigitalTwinsInstance by InputObject</span></span>
```powershell
PS C:\> $GetAzDigitalTwins =  Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsInstance -InputObject $GetAzDigitalTwins


```

<span data-ttu-id="ddc1d-113">Este comando remove um AzDigitalTwinsInstance pelo nome</span><span class="sxs-lookup"><span data-stu-id="ddc1d-113">This command removes an AzDigitalTwinsInstance by name</span></span>

## <span data-ttu-id="ddc1d-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ddc1d-114">PARAMETERS</span></span>

### <span data-ttu-id="ddc1d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddc1d-115">-AsJob</span></span>
<span data-ttu-id="ddc1d-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="ddc1d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ddc1d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc1d-117">-DefaultProfile</span></span>
<span data-ttu-id="ddc1d-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ddc1d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddc1d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddc1d-119">-InputObject</span></span>
<span data-ttu-id="ddc1d-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ddc1d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ddc1d-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ddc1d-121">-NoWait</span></span>
<span data-ttu-id="ddc1d-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="ddc1d-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ddc1d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ddc1d-123">-PassThru</span></span>
<span data-ttu-id="ddc1d-124">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="ddc1d-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ddc1d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc1d-125">-ResourceGroupName</span></span>
<span data-ttu-id="ddc1d-126">O nome do grupo de recursos que contém DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ddc1d-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="ddc1d-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ddc1d-127">-ResourceName</span></span>
<span data-ttu-id="ddc1d-128">O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ddc1d-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="ddc1d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ddc1d-129">-SubscriptionId</span></span>
<span data-ttu-id="ddc1d-130">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="ddc1d-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="ddc1d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddc1d-131">-Confirm</span></span>
<span data-ttu-id="ddc1d-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddc1d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddc1d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddc1d-133">-WhatIf</span></span>
<span data-ttu-id="ddc1d-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ddc1d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddc1d-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ddc1d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddc1d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc1d-136">CommonParameters</span></span>
<span data-ttu-id="ddc1d-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddc1d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc1d-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddc1d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc1d-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ddc1d-139">INPUTS</span></span>

### <span data-ttu-id="ddc1d-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="ddc1d-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="ddc1d-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ddc1d-141">OUTPUTS</span></span>

### <span data-ttu-id="ddc1d-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="ddc1d-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="ddc1d-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="ddc1d-143">NOTES</span></span>

<span data-ttu-id="ddc1d-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ddc1d-144">ALIASES</span></span>

<span data-ttu-id="ddc1d-145">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="ddc1d-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ddc1d-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ddc1d-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ddc1d-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ddc1d-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ddc1d-148">INPUTOBJECT <IDigitalTwinsIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="ddc1d-148">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ddc1d-149">`[EndpointName <String>]`: Nome do Recurso do Ponto de Extremidade.</span><span class="sxs-lookup"><span data-stu-id="ddc1d-149">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="ddc1d-150">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ddc1d-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ddc1d-151">`[Location <String>]`: Local de DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ddc1d-151">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="ddc1d-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ddc1d-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="ddc1d-153">`[ResourceName <String>]`: O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ddc1d-153">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="ddc1d-154">`[SubscriptionId <String>]`: O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="ddc1d-154">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="ddc1d-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ddc1d-155">RELATED LINKS</span></span>

