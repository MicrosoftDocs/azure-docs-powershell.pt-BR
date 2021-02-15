---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
ms.openlocfilehash: 495fecf922bc27eb43849b7ba6e44793c572b8cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113844"
---
# <span data-ttu-id="bbfd0-101">Remove-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="bbfd0-101">Remove-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="bbfd0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bbfd0-102">SYNOPSIS</span></span>
<span data-ttu-id="bbfd0-103">Exclua uma DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="bbfd0-103">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="bbfd0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbfd0-104">SYNTAX</span></span>

### <span data-ttu-id="bbfd0-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bbfd0-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bbfd0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bbfd0-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bbfd0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbfd0-107">DESCRIPTION</span></span>
<span data-ttu-id="bbfd0-108">Exclua uma DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="bbfd0-108">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="bbfd0-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bbfd0-109">EXAMPLES</span></span>

### <span data-ttu-id="bbfd0-110">Exemplo 1: Remover um AzDigitalTwinsInstance por nome</span><span class="sxs-lookup"><span data-stu-id="bbfd0-110">Example 1: Remove an AzDigitalTwinsInstance by name</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin


```

<span data-ttu-id="bbfd0-111">Este comando remove um AzDigitalTwinsInstance por nome</span><span class="sxs-lookup"><span data-stu-id="bbfd0-111">This command removes an AzDigitalTwinsInstance by name</span></span>

### <span data-ttu-id="bbfd0-112">Exemplo 2: Remover um AzDigitalTwinsInstance por InputObject</span><span class="sxs-lookup"><span data-stu-id="bbfd0-112">Example 2: Remove an AzDigitalTwinsInstance by InputObject</span></span>
```powershell
PS C:\> $GetAzDigitalTwins =  Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsInstance -InputObject $GetAzDigitalTwins


```

<span data-ttu-id="bbfd0-113">Este comando remove um AzDigitalTwinsInstance por nome</span><span class="sxs-lookup"><span data-stu-id="bbfd0-113">This command removes an AzDigitalTwinsInstance by name</span></span>

## <span data-ttu-id="bbfd0-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbfd0-114">PARAMETERS</span></span>

### <span data-ttu-id="bbfd0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbfd0-115">-AsJob</span></span>
<span data-ttu-id="bbfd0-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="bbfd0-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bbfd0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbfd0-117">-DefaultProfile</span></span>
<span data-ttu-id="bbfd0-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bbfd0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbfd0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbfd0-119">-InputObject</span></span>
<span data-ttu-id="bbfd0-120">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="bbfd0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bbfd0-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bbfd0-121">-NoWait</span></span>
<span data-ttu-id="bbfd0-122">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="bbfd0-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bbfd0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbfd0-123">-PassThru</span></span>
<span data-ttu-id="bbfd0-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="bbfd0-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bbfd0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbfd0-125">-ResourceGroupName</span></span>
<span data-ttu-id="bbfd0-126">O nome do grupo de recursos que contém a DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="bbfd0-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="bbfd0-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bbfd0-127">-ResourceName</span></span>
<span data-ttu-id="bbfd0-128">O nome da DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="bbfd0-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="bbfd0-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bbfd0-129">-SubscriptionId</span></span>
<span data-ttu-id="bbfd0-130">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="bbfd0-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="bbfd0-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bbfd0-131">-Confirm</span></span>
<span data-ttu-id="bbfd0-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbfd0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbfd0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbfd0-133">-WhatIf</span></span>
<span data-ttu-id="bbfd0-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bbfd0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbfd0-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bbfd0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbfd0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbfd0-136">CommonParameters</span></span>
<span data-ttu-id="bbfd0-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbfd0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbfd0-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbfd0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbfd0-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="bbfd0-139">INPUTS</span></span>

### <span data-ttu-id="bbfd0-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="bbfd0-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="bbfd0-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="bbfd0-141">OUTPUTS</span></span>

### <span data-ttu-id="bbfd0-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="bbfd0-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="bbfd0-143">Notas</span><span class="sxs-lookup"><span data-stu-id="bbfd0-143">NOTES</span></span>

<span data-ttu-id="bbfd0-144">Aliases</span><span class="sxs-lookup"><span data-stu-id="bbfd0-144">ALIASES</span></span>

<span data-ttu-id="bbfd0-145">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="bbfd0-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bbfd0-146">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="bbfd0-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bbfd0-147">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bbfd0-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bbfd0-148">INPUTOBJECT: <IDigitalTwinsIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="bbfd0-148">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bbfd0-149">`[EndpointName <String>]`: Nome do Recurso do Ponto de Extremidade.</span><span class="sxs-lookup"><span data-stu-id="bbfd0-149">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="bbfd0-150">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="bbfd0-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bbfd0-151">`[Location <String>]`: Localização do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="bbfd0-151">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="bbfd0-152">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="bbfd0-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="bbfd0-153">`[ResourceName <String>]`: o nome da DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="bbfd0-153">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="bbfd0-154">`[SubscriptionId <String>]`: o identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="bbfd0-154">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="bbfd0-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbfd0-155">RELATED LINKS</span></span>

