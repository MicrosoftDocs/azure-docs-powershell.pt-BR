---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 4b8bd90cd96654fa137301379dceaabccad8a2ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111989"
---
# <span data-ttu-id="d8702-101">New-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="d8702-101">New-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="d8702-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8702-102">SYNOPSIS</span></span>
<span data-ttu-id="d8702-103">Cria uma nova ordem para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8702-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="d8702-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8702-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8702-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8702-105">DESCRIPTION</span></span>
<span data-ttu-id="d8702-106">O **cmdlet New-AzDataBoxEdgeOrder** cria uma nova ordem para um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="d8702-106">The **New-AzDataBoxEdgeOrder** cmdlet creates a new order for a Data Box Edge device.</span></span> <span data-ttu-id="d8702-107">Um recurso de dispositivo de borda de caixa de dados precisa ser criado primeiro antes de criar uma ordem.</span><span class="sxs-lookup"><span data-stu-id="d8702-107">A Data Box Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="d8702-108">Você pode especificar detalhes como contato, nome da empresa, email, endereço etc. como parâmetros para criar o pedido.</span><span class="sxs-lookup"><span data-stu-id="d8702-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="d8702-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d8702-109">EXAMPLES</span></span>

### <span data-ttu-id="d8702-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d8702-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="d8702-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8702-111">PARAMETERS</span></span>

### <span data-ttu-id="d8702-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="d8702-112">-AddressLine1</span></span>
<span data-ttu-id="d8702-113">Endereço primeira linha</span><span class="sxs-lookup"><span data-stu-id="d8702-113">Address first line</span></span>

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

### <span data-ttu-id="d8702-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="d8702-114">-AddressLine2</span></span>
<span data-ttu-id="d8702-115">Endereço segunda linha</span><span class="sxs-lookup"><span data-stu-id="d8702-115">Address second line</span></span>

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

### <span data-ttu-id="d8702-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="d8702-116">-AddressLine3</span></span>
<span data-ttu-id="d8702-117">Endereço terceira linha</span><span class="sxs-lookup"><span data-stu-id="d8702-117">Address third line</span></span>

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

### <span data-ttu-id="d8702-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8702-118">-AsJob</span></span>
<span data-ttu-id="d8702-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d8702-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8702-120">-Cidade</span><span class="sxs-lookup"><span data-stu-id="d8702-120">-City</span></span>
<span data-ttu-id="d8702-121">Nome da Cidade</span><span class="sxs-lookup"><span data-stu-id="d8702-121">Name of the City</span></span>

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

### <span data-ttu-id="d8702-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="d8702-122">-CompanyName</span></span>
<span data-ttu-id="d8702-123">Nome da empresa</span><span class="sxs-lookup"><span data-stu-id="d8702-123">Name of the company</span></span>

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

### <span data-ttu-id="d8702-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="d8702-124">-ContactPerson</span></span>
<span data-ttu-id="d8702-125">Nome da pessoa de contato</span><span class="sxs-lookup"><span data-stu-id="d8702-125">Name of the contact person</span></span>

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

### <span data-ttu-id="d8702-126">-País/Região</span><span class="sxs-lookup"><span data-stu-id="d8702-126">-Country</span></span>
<span data-ttu-id="d8702-127">Nome do País</span><span class="sxs-lookup"><span data-stu-id="d8702-127">Name of the Country</span></span>

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

### <span data-ttu-id="d8702-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8702-128">-DefaultProfile</span></span>
<span data-ttu-id="d8702-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8702-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8702-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d8702-130">-DeviceName</span></span>
<span data-ttu-id="d8702-131">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="d8702-131">Resource Name</span></span>

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

### <span data-ttu-id="d8702-132">-Email</span><span class="sxs-lookup"><span data-stu-id="d8702-132">-Email</span></span>
<span data-ttu-id="d8702-133">Lista de Emails para receber atualizações, Aceita no máximo 10 emails</span><span class="sxs-lookup"><span data-stu-id="d8702-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="d8702-134">-Telefone</span><span class="sxs-lookup"><span data-stu-id="d8702-134">-Phone</span></span>
<span data-ttu-id="d8702-135">Número de telefone do contato</span><span class="sxs-lookup"><span data-stu-id="d8702-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="d8702-136">-Cep</span><span class="sxs-lookup"><span data-stu-id="d8702-136">-PostalCode</span></span>
<span data-ttu-id="d8702-137">CEP do Endereço</span><span class="sxs-lookup"><span data-stu-id="d8702-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="d8702-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8702-138">-ResourceGroupName</span></span>
<span data-ttu-id="d8702-139">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d8702-139">Resource Group Name</span></span>

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

### <span data-ttu-id="d8702-140">-Estado</span><span class="sxs-lookup"><span data-stu-id="d8702-140">-State</span></span>
<span data-ttu-id="d8702-141">Nome do Estado</span><span class="sxs-lookup"><span data-stu-id="d8702-141">Name of the State</span></span>

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

### <span data-ttu-id="d8702-142">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d8702-142">-Confirm</span></span>
<span data-ttu-id="d8702-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8702-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8702-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8702-144">-WhatIf</span></span>
<span data-ttu-id="d8702-145">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d8702-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8702-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8702-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8702-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8702-147">CommonParameters</span></span>
<span data-ttu-id="d8702-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8702-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8702-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8702-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8702-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="d8702-150">INPUTS</span></span>

### <span data-ttu-id="d8702-151">System.String</span><span class="sxs-lookup"><span data-stu-id="d8702-151">System.String</span></span>

## <span data-ttu-id="d8702-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="d8702-152">OUTPUTS</span></span>

### <span data-ttu-id="d8702-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="d8702-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="d8702-154">Notas</span><span class="sxs-lookup"><span data-stu-id="d8702-154">NOTES</span></span>

## <span data-ttu-id="d8702-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8702-155">RELATED LINKS</span></span>
