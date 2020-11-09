---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 4b8bd90cd96654fa137301379dceaabccad8a2ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281143"
---
# <span data-ttu-id="f8aec-101">New-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="f8aec-101">New-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="f8aec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8aec-102">SYNOPSIS</span></span>
<span data-ttu-id="f8aec-103">Cria um novo pedido para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8aec-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="f8aec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8aec-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8aec-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8aec-105">DESCRIPTION</span></span>
<span data-ttu-id="f8aec-106">O cmdlet **New-AzDataBoxEdgeOrder** cria um novo pedido para um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="f8aec-106">The **New-AzDataBoxEdgeOrder** cmdlet creates a new order for a Data Box Edge device.</span></span> <span data-ttu-id="f8aec-107">Um recurso de dispositivo de borda de caixa de dados precisa ser criado primeiro antes de criar um pedido.</span><span class="sxs-lookup"><span data-stu-id="f8aec-107">A Data Box Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="f8aec-108">Você pode especificar detalhes como pessoa de contato, nome da empresa, email, endereço, etc. como parâmetros para criar o pedido.</span><span class="sxs-lookup"><span data-stu-id="f8aec-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="f8aec-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8aec-109">EXAMPLES</span></span>

### <span data-ttu-id="f8aec-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f8aec-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="f8aec-111">OS</span><span class="sxs-lookup"><span data-stu-id="f8aec-111">PARAMETERS</span></span>

### <span data-ttu-id="f8aec-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="f8aec-112">-AddressLine1</span></span>
<span data-ttu-id="f8aec-113">Primeira linha de endereço</span><span class="sxs-lookup"><span data-stu-id="f8aec-113">Address first line</span></span>

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

### <span data-ttu-id="f8aec-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="f8aec-114">-AddressLine2</span></span>
<span data-ttu-id="f8aec-115">Endereço segunda linha</span><span class="sxs-lookup"><span data-stu-id="f8aec-115">Address second line</span></span>

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

### <span data-ttu-id="f8aec-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="f8aec-116">-AddressLine3</span></span>
<span data-ttu-id="f8aec-117">Endereço-terceira linha</span><span class="sxs-lookup"><span data-stu-id="f8aec-117">Address third line</span></span>

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

### <span data-ttu-id="f8aec-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8aec-118">-AsJob</span></span>
<span data-ttu-id="f8aec-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f8aec-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8aec-120">-Cidade</span><span class="sxs-lookup"><span data-stu-id="f8aec-120">-City</span></span>
<span data-ttu-id="f8aec-121">Nome da cidade</span><span class="sxs-lookup"><span data-stu-id="f8aec-121">Name of the City</span></span>

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

### <span data-ttu-id="f8aec-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="f8aec-122">-CompanyName</span></span>
<span data-ttu-id="f8aec-123">Nome da empresa</span><span class="sxs-lookup"><span data-stu-id="f8aec-123">Name of the company</span></span>

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

### <span data-ttu-id="f8aec-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="f8aec-124">-ContactPerson</span></span>
<span data-ttu-id="f8aec-125">Nome da pessoa de contato</span><span class="sxs-lookup"><span data-stu-id="f8aec-125">Name of the contact person</span></span>

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

### <span data-ttu-id="f8aec-126">-País</span><span class="sxs-lookup"><span data-stu-id="f8aec-126">-Country</span></span>
<span data-ttu-id="f8aec-127">Nome do país</span><span class="sxs-lookup"><span data-stu-id="f8aec-127">Name of the Country</span></span>

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

### <span data-ttu-id="f8aec-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8aec-128">-DefaultProfile</span></span>
<span data-ttu-id="f8aec-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8aec-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8aec-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f8aec-130">-DeviceName</span></span>
<span data-ttu-id="f8aec-131">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="f8aec-131">Resource Name</span></span>

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

### <span data-ttu-id="f8aec-132">-Email</span><span class="sxs-lookup"><span data-stu-id="f8aec-132">-Email</span></span>
<span data-ttu-id="f8aec-133">Lista de emails para receber atualizações, aceita o máximo de 10 emails</span><span class="sxs-lookup"><span data-stu-id="f8aec-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="f8aec-134">-Telefone</span><span class="sxs-lookup"><span data-stu-id="f8aec-134">-Phone</span></span>
<span data-ttu-id="f8aec-135">Número de telefone da pessoa de contato</span><span class="sxs-lookup"><span data-stu-id="f8aec-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="f8aec-136">-CEP</span><span class="sxs-lookup"><span data-stu-id="f8aec-136">-PostalCode</span></span>
<span data-ttu-id="f8aec-137">Código postal do endereço</span><span class="sxs-lookup"><span data-stu-id="f8aec-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="f8aec-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8aec-138">-ResourceGroupName</span></span>
<span data-ttu-id="f8aec-139">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f8aec-139">Resource Group Name</span></span>

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

### <span data-ttu-id="f8aec-140">-Estado</span><span class="sxs-lookup"><span data-stu-id="f8aec-140">-State</span></span>
<span data-ttu-id="f8aec-141">Nome do estado</span><span class="sxs-lookup"><span data-stu-id="f8aec-141">Name of the State</span></span>

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

### <span data-ttu-id="f8aec-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f8aec-142">-Confirm</span></span>
<span data-ttu-id="f8aec-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8aec-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8aec-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8aec-144">-WhatIf</span></span>
<span data-ttu-id="f8aec-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f8aec-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8aec-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f8aec-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8aec-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8aec-147">CommonParameters</span></span>
<span data-ttu-id="f8aec-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8aec-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8aec-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8aec-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8aec-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8aec-150">INPUTS</span></span>

### <span data-ttu-id="f8aec-151">System. String</span><span class="sxs-lookup"><span data-stu-id="f8aec-151">System.String</span></span>

## <span data-ttu-id="f8aec-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8aec-152">OUTPUTS</span></span>

### <span data-ttu-id="f8aec-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="f8aec-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="f8aec-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8aec-154">NOTES</span></span>

## <span data-ttu-id="f8aec-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8aec-155">RELATED LINKS</span></span>
