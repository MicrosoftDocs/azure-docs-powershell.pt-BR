---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverbulkremove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverBulkRemove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverBulkRemove.md
ms.openlocfilehash: f9815c32526a5ce462a50ec167771d30bc840b1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891650"
---
# <span data-ttu-id="62bcf-101">Invoke-AzResourceMoverBulkRemove</span><span class="sxs-lookup"><span data-stu-id="62bcf-101">Invoke-AzResourceMoverBulkRemove</span></span>

## <span data-ttu-id="62bcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="62bcf-103">Remove o conjunto de recursos de movimentação incluídos no corpo da solicitação da coleção move.</span><span class="sxs-lookup"><span data-stu-id="62bcf-103">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="62bcf-104">A orquestração é feita por serviço.</span><span class="sxs-lookup"><span data-stu-id="62bcf-104">The orchestration is done by service.</span></span>
<span data-ttu-id="62bcf-105">Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="62bcf-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="62bcf-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="62bcf-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverBulkRemove -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-MoveResource <String[]>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="62bcf-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="62bcf-107">DESCRIPTION</span></span>
<span data-ttu-id="62bcf-108">Remove o conjunto de recursos de movimentação incluídos no corpo da solicitação da coleção move.</span><span class="sxs-lookup"><span data-stu-id="62bcf-108">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="62bcf-109">A orquestração é feita por serviço.</span><span class="sxs-lookup"><span data-stu-id="62bcf-109">The orchestration is done by service.</span></span>
<span data-ttu-id="62bcf-110">Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="62bcf-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="62bcf-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62bcf-111">EXAMPLES</span></span>

### <span data-ttu-id="62bcf-112">Exemplo 1: Validar as dependentes antes de remover os Recursos de Movimentação da Coleção Move</span><span class="sxs-lookup"><span data-stu-id="62bcf-112">Example 1: Validate the dependecies before remove of the Move Resources from Move Collection</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:52:28 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/b4e3f140-b36b-4fd5-a507-b1e663ecf7a3
Message        : 
Name           : b4e3f140-b36b-4fd5-a507-b1e663ecf7a3
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:52:28 PM
Status         : Succeeded

```

<span data-ttu-id="62bcf-113">Valide as dependeções antes de remover os recursos de movimentação da Coleção Move.</span><span class="sxs-lookup"><span data-stu-id="62bcf-113">Validate the dependecies before remove of the move resources from Move Collection.</span></span>

### <span data-ttu-id="62bcf-114">Exemplo 2: Remover o recurso Move da coleção Move usando "Nome do MoveResource" como entrada</span><span class="sxs-lookup"><span data-stu-id="62bcf-114">Example 2: Remove the Move Resource from Move Collection using "MoveResource Name" as input</span></span>
```powershell
Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:58:10 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/d4827071-b797-45c5-b88c-00ddd7818d42
Message        : 
Name           : d4827071-b797-45c5-b88c-00ddd7818d42
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:57:08 PM
Status         : Succeeded
```

<span data-ttu-id="62bcf-115">Remover o Recurso de Movimentação da Coleção Move usando "MoveResource Name" como entrada</span><span class="sxs-lookup"><span data-stu-id="62bcf-115">Remove the Move Resource from Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="62bcf-116">Exemplo 3: Remover o recurso Move da coleção Move usando "SourceARMID" como entrada</span><span class="sxs-lookup"><span data-stu-id="62bcf-116">Example 3: Remove the Move Resource from Move Collection using "SourceARMID" as input</span></span>
```powershell
Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:05:13 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/7b6904e2-fc3f-400d-b248-8908fcb282fb
Message        : 
Name           : 7b6904e2-fc3f-400d-b248-8908fcb282fb
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:05:00 PM
Status         : Succeeded
```

<span data-ttu-id="62bcf-117">Remover o recurso Mover da Coleção Move usando "SourceARMID" como entrada</span><span class="sxs-lookup"><span data-stu-id="62bcf-117">Remove the Move Resource from Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="62bcf-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="62bcf-118">PARAMETERS</span></span>

### <span data-ttu-id="62bcf-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62bcf-119">-AsJob</span></span>
<span data-ttu-id="62bcf-120">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="62bcf-120">Run the command as a job</span></span>

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

### <span data-ttu-id="62bcf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62bcf-121">-DefaultProfile</span></span>
<span data-ttu-id="62bcf-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62bcf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62bcf-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="62bcf-123">-MoveCollectionName</span></span>
<span data-ttu-id="62bcf-124">.</span><span class="sxs-lookup"><span data-stu-id="62bcf-124">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bcf-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="62bcf-125">-MoveResource</span></span>
<span data-ttu-id="62bcf-126">Obtém ou define a lista de IDs de recursos, por padrão, aceita mover ids de recurso, a menos que o tipo de entrada seja comutado por meio da propriedade moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="62bcf-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bcf-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="62bcf-127">-MoveResourceInputType</span></span>
<span data-ttu-id="62bcf-128">Define o tipo de entrada de recurso move.</span><span class="sxs-lookup"><span data-stu-id="62bcf-128">Defines the move resource input type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.MoveResourceInputType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bcf-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="62bcf-129">-NoWait</span></span>
<span data-ttu-id="62bcf-130">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="62bcf-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="62bcf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62bcf-131">-ResourceGroupName</span></span>
<span data-ttu-id="62bcf-132">.</span><span class="sxs-lookup"><span data-stu-id="62bcf-132">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bcf-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62bcf-133">-SubscriptionId</span></span>
<span data-ttu-id="62bcf-134">A ID da Assinatura.</span><span class="sxs-lookup"><span data-stu-id="62bcf-134">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bcf-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="62bcf-135">-ValidateOnly</span></span>
<span data-ttu-id="62bcf-136">Obtém ou define um valor que indica se a operação precisa executar somente pré-requisito.</span><span class="sxs-lookup"><span data-stu-id="62bcf-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="62bcf-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62bcf-137">-Confirm</span></span>
<span data-ttu-id="62bcf-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62bcf-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62bcf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62bcf-139">-WhatIf</span></span>
<span data-ttu-id="62bcf-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="62bcf-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62bcf-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="62bcf-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62bcf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62bcf-142">CommonParameters</span></span>
<span data-ttu-id="62bcf-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62bcf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62bcf-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62bcf-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62bcf-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62bcf-145">INPUTS</span></span>

## <span data-ttu-id="62bcf-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="62bcf-146">OUTPUTS</span></span>

### <span data-ttu-id="62bcf-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="62bcf-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="62bcf-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="62bcf-148">NOTES</span></span>

<span data-ttu-id="62bcf-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="62bcf-149">ALIASES</span></span>

## <span data-ttu-id="62bcf-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62bcf-150">RELATED LINKS</span></span>

