---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
ms.openlocfilehash: 4cb6c46f3cadae9d36ec273fe7d6198e35927c81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889134"
---
# <span data-ttu-id="9c470-101">New-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="9c470-101">New-AzStackEdgeOrder</span></span>

## <span data-ttu-id="9c470-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c470-102">SYNOPSIS</span></span>
<span data-ttu-id="9c470-103">Cria uma nova ordem para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c470-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="9c470-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9c470-104">SYNTAX</span></span>

```
New-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c470-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9c470-105">DESCRIPTION</span></span>
<span data-ttu-id="9c470-106">O cmdlet **New-AzStackEdgeOrder** cria uma nova ordem para um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="9c470-106">The **New-AzStackEdgeOrder** cmdlet creates a new order for a Stack Edge device.</span></span> <span data-ttu-id="9c470-107">Um recurso de dispositivo de Borda de Pilha precisa ser criado primeiro antes de criar uma ordem.</span><span class="sxs-lookup"><span data-stu-id="9c470-107">A Stack Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="9c470-108">Você pode especificar detalhes como pessoa de contato, nome da empresa, email, endereço etc. como parâmetros para a criação do pedido.</span><span class="sxs-lookup"><span data-stu-id="9c470-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="9c470-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c470-109">EXAMPLES</span></span>

### <span data-ttu-id="9c470-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c470-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="9c470-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9c470-111">PARAMETERS</span></span>

### <span data-ttu-id="9c470-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="9c470-112">-AddressLine1</span></span>
<span data-ttu-id="9c470-113">Primeira linha de endereço</span><span class="sxs-lookup"><span data-stu-id="9c470-113">Address first line</span></span>

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

### <span data-ttu-id="9c470-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="9c470-114">-AddressLine2</span></span>
<span data-ttu-id="9c470-115">Endereço segunda linha</span><span class="sxs-lookup"><span data-stu-id="9c470-115">Address second line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c470-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="9c470-116">-AddressLine3</span></span>
<span data-ttu-id="9c470-117">Endereço terceira linha</span><span class="sxs-lookup"><span data-stu-id="9c470-117">Address third line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c470-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c470-118">-AsJob</span></span>
<span data-ttu-id="9c470-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9c470-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c470-120">-City</span><span class="sxs-lookup"><span data-stu-id="9c470-120">-City</span></span>
<span data-ttu-id="9c470-121">Nome da cidade</span><span class="sxs-lookup"><span data-stu-id="9c470-121">Name of the City</span></span>

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

### <span data-ttu-id="9c470-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="9c470-122">-CompanyName</span></span>
<span data-ttu-id="9c470-123">Nome da empresa</span><span class="sxs-lookup"><span data-stu-id="9c470-123">Name of the company</span></span>

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

### <span data-ttu-id="9c470-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="9c470-124">-ContactPerson</span></span>
<span data-ttu-id="9c470-125">Nome da pessoa de contato</span><span class="sxs-lookup"><span data-stu-id="9c470-125">Name of the contact person</span></span>

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

### <span data-ttu-id="9c470-126">-Country</span><span class="sxs-lookup"><span data-stu-id="9c470-126">-Country</span></span>
<span data-ttu-id="9c470-127">Nome do país</span><span class="sxs-lookup"><span data-stu-id="9c470-127">Name of the Country</span></span>

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

### <span data-ttu-id="9c470-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c470-128">-DefaultProfile</span></span>
<span data-ttu-id="9c470-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c470-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c470-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9c470-130">-DeviceName</span></span>
<span data-ttu-id="9c470-131">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="9c470-131">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c470-132">-Email</span><span class="sxs-lookup"><span data-stu-id="9c470-132">-Email</span></span>
<span data-ttu-id="9c470-133">Lista de emails para receber atualizações, Aceita no máximo 10 emails</span><span class="sxs-lookup"><span data-stu-id="9c470-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c470-134">-Phone</span><span class="sxs-lookup"><span data-stu-id="9c470-134">-Phone</span></span>
<span data-ttu-id="9c470-135">Número de telefone da pessoa de contato</span><span class="sxs-lookup"><span data-stu-id="9c470-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="9c470-136">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="9c470-136">-PostalCode</span></span>
<span data-ttu-id="9c470-137">Código Postal do Endereço</span><span class="sxs-lookup"><span data-stu-id="9c470-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="9c470-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c470-138">-ResourceGroupName</span></span>
<span data-ttu-id="9c470-139">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="9c470-139">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c470-140">-State</span><span class="sxs-lookup"><span data-stu-id="9c470-140">-State</span></span>
<span data-ttu-id="9c470-141">Nome do Estado</span><span class="sxs-lookup"><span data-stu-id="9c470-141">Name of the State</span></span>

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

### <span data-ttu-id="9c470-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c470-142">-Confirm</span></span>
<span data-ttu-id="9c470-143">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c470-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c470-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c470-144">-WhatIf</span></span>
<span data-ttu-id="9c470-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c470-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c470-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c470-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c470-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c470-147">CommonParameters</span></span>
<span data-ttu-id="9c470-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c470-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c470-149">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c470-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c470-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c470-150">INPUTS</span></span>

### <span data-ttu-id="9c470-151">System.String</span><span class="sxs-lookup"><span data-stu-id="9c470-151">System.String</span></span>

## <span data-ttu-id="9c470-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9c470-152">OUTPUTS</span></span>

### <span data-ttu-id="9c470-153">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="9c470-153">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="9c470-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="9c470-154">NOTES</span></span>

## <span data-ttu-id="9c470-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c470-155">RELATED LINKS</span></span>
