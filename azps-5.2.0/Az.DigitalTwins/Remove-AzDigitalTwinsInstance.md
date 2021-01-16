---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
ms.openlocfilehash: 495fecf922bc27eb43849b7ba6e44793c572b8cd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260539"
---
# <span data-ttu-id="406e3-101">Remove-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="406e3-101">Remove-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="406e3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="406e3-102">SYNOPSIS</span></span>
<span data-ttu-id="406e3-103">Excluir um DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="406e3-103">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="406e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="406e3-104">SYNTAX</span></span>

### <span data-ttu-id="406e3-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="406e3-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="406e3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="406e3-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="406e3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="406e3-107">DESCRIPTION</span></span>
<span data-ttu-id="406e3-108">Excluir um DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="406e3-108">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="406e3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="406e3-109">EXAMPLES</span></span>

### <span data-ttu-id="406e3-110">Exemplo 1: remover um AzDigitalTwinsInstance por nome</span><span class="sxs-lookup"><span data-stu-id="406e3-110">Example 1: Remove an AzDigitalTwinsInstance by name</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin


```

<span data-ttu-id="406e3-111">Este comando Remove um AzDigitalTwinsInstance por nome</span><span class="sxs-lookup"><span data-stu-id="406e3-111">This command removes an AzDigitalTwinsInstance by name</span></span>

### <span data-ttu-id="406e3-112">Exemplo 2: remover um AzDigitalTwinsInstance por InputObject</span><span class="sxs-lookup"><span data-stu-id="406e3-112">Example 2: Remove an AzDigitalTwinsInstance by InputObject</span></span>
```powershell
PS C:\> $GetAzDigitalTwins =  Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsInstance -InputObject $GetAzDigitalTwins


```

<span data-ttu-id="406e3-113">Este comando Remove um AzDigitalTwinsInstance por nome</span><span class="sxs-lookup"><span data-stu-id="406e3-113">This command removes an AzDigitalTwinsInstance by name</span></span>

## <span data-ttu-id="406e3-114">OS</span><span class="sxs-lookup"><span data-stu-id="406e3-114">PARAMETERS</span></span>

### <span data-ttu-id="406e3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="406e3-115">-AsJob</span></span>
<span data-ttu-id="406e3-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="406e3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="406e3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="406e3-117">-DefaultProfile</span></span>
<span data-ttu-id="406e3-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="406e3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="406e3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="406e3-119">-InputObject</span></span>
<span data-ttu-id="406e3-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="406e3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="406e3-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="406e3-121">-NoWait</span></span>
<span data-ttu-id="406e3-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="406e3-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="406e3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="406e3-123">-PassThru</span></span>
<span data-ttu-id="406e3-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="406e3-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="406e3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="406e3-125">-ResourceGroupName</span></span>
<span data-ttu-id="406e3-126">O nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="406e3-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="406e3-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="406e3-127">-ResourceName</span></span>
<span data-ttu-id="406e3-128">O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="406e3-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="406e3-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="406e3-129">-SubscriptionId</span></span>
<span data-ttu-id="406e3-130">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="406e3-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="406e3-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="406e3-131">-Confirm</span></span>
<span data-ttu-id="406e3-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="406e3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="406e3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="406e3-133">-WhatIf</span></span>
<span data-ttu-id="406e3-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="406e3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="406e3-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="406e3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="406e3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="406e3-136">CommonParameters</span></span>
<span data-ttu-id="406e3-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="406e3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="406e3-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="406e3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="406e3-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="406e3-139">INPUTS</span></span>

### <span data-ttu-id="406e3-140">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="406e3-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="406e3-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="406e3-141">OUTPUTS</span></span>

### <span data-ttu-id="406e3-142">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="406e3-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="406e3-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="406e3-143">NOTES</span></span>

<span data-ttu-id="406e3-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="406e3-144">ALIASES</span></span>

<span data-ttu-id="406e3-145">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="406e3-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="406e3-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="406e3-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="406e3-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="406e3-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="406e3-148">INPUTobject <IDigitalTwinsIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="406e3-148">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="406e3-149">`[EndpointName <String>]`: Nome do recurso de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="406e3-149">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="406e3-150">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="406e3-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="406e3-151">`[Location <String>]`: Local do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="406e3-151">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="406e3-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="406e3-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="406e3-153">`[ResourceName <String>]`: O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="406e3-153">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="406e3-154">`[SubscriptionId <String>]`: O identificador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="406e3-154">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="406e3-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="406e3-155">RELATED LINKS</span></span>

