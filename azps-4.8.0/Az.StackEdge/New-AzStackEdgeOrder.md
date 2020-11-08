---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
ms.openlocfilehash: a39986404e0969de2db4a2b58e0d275e102799cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113217"
---
# <span data-ttu-id="04442-101">New-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="04442-101">New-AzStackEdgeOrder</span></span>

## <span data-ttu-id="04442-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04442-102">SYNOPSIS</span></span>
<span data-ttu-id="04442-103">Cria um novo pedido para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="04442-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="04442-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04442-104">SYNTAX</span></span>

```
New-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04442-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04442-105">DESCRIPTION</span></span>
<span data-ttu-id="04442-106">O cmdlet **New-AzStackEdgeOrder** cria um novo pedido para um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="04442-106">The **New-AzStackEdgeOrder** cmdlet creates a new order for a Stack Edge device.</span></span> <span data-ttu-id="04442-107">Um recurso de dispositivo de borda de pilha precisa ser criado primeiro antes da criação de um pedido.</span><span class="sxs-lookup"><span data-stu-id="04442-107">A Stack Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="04442-108">Você pode especificar detalhes como pessoa de contato, nome da empresa, email, endereço, etc. como parâmetros para criar o pedido.</span><span class="sxs-lookup"><span data-stu-id="04442-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="04442-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04442-109">EXAMPLES</span></span>

### <span data-ttu-id="04442-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="04442-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="04442-111">OS</span><span class="sxs-lookup"><span data-stu-id="04442-111">PARAMETERS</span></span>

### <span data-ttu-id="04442-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="04442-112">-AddressLine1</span></span>
<span data-ttu-id="04442-113">Primeira linha de endereço</span><span class="sxs-lookup"><span data-stu-id="04442-113">Address first line</span></span>

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

### <span data-ttu-id="04442-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="04442-114">-AddressLine2</span></span>
<span data-ttu-id="04442-115">Endereço segunda linha</span><span class="sxs-lookup"><span data-stu-id="04442-115">Address second line</span></span>

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

### <span data-ttu-id="04442-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="04442-116">-AddressLine3</span></span>
<span data-ttu-id="04442-117">Endereço-terceira linha</span><span class="sxs-lookup"><span data-stu-id="04442-117">Address third line</span></span>

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

### <span data-ttu-id="04442-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04442-118">-AsJob</span></span>
<span data-ttu-id="04442-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="04442-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04442-120">-Cidade</span><span class="sxs-lookup"><span data-stu-id="04442-120">-City</span></span>
<span data-ttu-id="04442-121">Nome da cidade</span><span class="sxs-lookup"><span data-stu-id="04442-121">Name of the City</span></span>

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

### <span data-ttu-id="04442-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="04442-122">-CompanyName</span></span>
<span data-ttu-id="04442-123">Nome da empresa</span><span class="sxs-lookup"><span data-stu-id="04442-123">Name of the company</span></span>

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

### <span data-ttu-id="04442-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="04442-124">-ContactPerson</span></span>
<span data-ttu-id="04442-125">Nome da pessoa de contato</span><span class="sxs-lookup"><span data-stu-id="04442-125">Name of the contact person</span></span>

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

### <span data-ttu-id="04442-126">-País</span><span class="sxs-lookup"><span data-stu-id="04442-126">-Country</span></span>
<span data-ttu-id="04442-127">Nome do país</span><span class="sxs-lookup"><span data-stu-id="04442-127">Name of the Country</span></span>

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

### <span data-ttu-id="04442-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04442-128">-DefaultProfile</span></span>
<span data-ttu-id="04442-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04442-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04442-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="04442-130">-DeviceName</span></span>
<span data-ttu-id="04442-131">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="04442-131">Resource Name</span></span>

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

### <span data-ttu-id="04442-132">-Email</span><span class="sxs-lookup"><span data-stu-id="04442-132">-Email</span></span>
<span data-ttu-id="04442-133">Lista de emails para receber atualizações, aceita o máximo de 10 emails</span><span class="sxs-lookup"><span data-stu-id="04442-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="04442-134">-Telefone</span><span class="sxs-lookup"><span data-stu-id="04442-134">-Phone</span></span>
<span data-ttu-id="04442-135">Número de telefone da pessoa de contato</span><span class="sxs-lookup"><span data-stu-id="04442-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="04442-136">-CEP</span><span class="sxs-lookup"><span data-stu-id="04442-136">-PostalCode</span></span>
<span data-ttu-id="04442-137">Código postal do endereço</span><span class="sxs-lookup"><span data-stu-id="04442-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="04442-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04442-138">-ResourceGroupName</span></span>
<span data-ttu-id="04442-139">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="04442-139">Resource Group Name</span></span>

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

### <span data-ttu-id="04442-140">-Estado</span><span class="sxs-lookup"><span data-stu-id="04442-140">-State</span></span>
<span data-ttu-id="04442-141">Nome do estado</span><span class="sxs-lookup"><span data-stu-id="04442-141">Name of the State</span></span>

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

### <span data-ttu-id="04442-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="04442-142">-Confirm</span></span>
<span data-ttu-id="04442-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04442-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04442-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04442-144">-WhatIf</span></span>
<span data-ttu-id="04442-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="04442-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04442-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="04442-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04442-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04442-147">CommonParameters</span></span>
<span data-ttu-id="04442-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04442-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04442-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04442-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04442-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04442-150">INPUTS</span></span>

### <span data-ttu-id="04442-151">System. String</span><span class="sxs-lookup"><span data-stu-id="04442-151">System.String</span></span>

## <span data-ttu-id="04442-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04442-152">OUTPUTS</span></span>

### <span data-ttu-id="04442-153">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="04442-153">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="04442-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04442-154">NOTES</span></span>

## <span data-ttu-id="04442-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04442-155">RELATED LINKS</span></span>
