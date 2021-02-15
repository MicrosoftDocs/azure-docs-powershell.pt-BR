---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
ms.openlocfilehash: a39986404e0969de2db4a2b58e0d275e102799cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118918"
---
# <span data-ttu-id="63067-101">New-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="63067-101">New-AzStackEdgeOrder</span></span>

## <span data-ttu-id="63067-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63067-102">SYNOPSIS</span></span>
<span data-ttu-id="63067-103">Cria uma nova ordem para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63067-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="63067-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63067-104">SYNTAX</span></span>

```
New-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63067-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="63067-105">DESCRIPTION</span></span>
<span data-ttu-id="63067-106">O **cmdlet New-AzSt stackEdgeOrder** cria uma nova ordem para um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="63067-106">The **New-AzStackEdgeOrder** cmdlet creates a new order for a Stack Edge device.</span></span> <span data-ttu-id="63067-107">Um recurso de dispositivo Stack Edge precisa ser criado primeiro antes de criar uma ordem.</span><span class="sxs-lookup"><span data-stu-id="63067-107">A Stack Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="63067-108">Você pode especificar detalhes como contato, nome da empresa, email, endereço etc. como parâmetros para criar o pedido.</span><span class="sxs-lookup"><span data-stu-id="63067-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="63067-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="63067-109">EXAMPLES</span></span>

### <span data-ttu-id="63067-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="63067-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="63067-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63067-111">PARAMETERS</span></span>

### <span data-ttu-id="63067-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="63067-112">-AddressLine1</span></span>
<span data-ttu-id="63067-113">Endereço primeira linha</span><span class="sxs-lookup"><span data-stu-id="63067-113">Address first line</span></span>

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

### <span data-ttu-id="63067-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="63067-114">-AddressLine2</span></span>
<span data-ttu-id="63067-115">Endereço segunda linha</span><span class="sxs-lookup"><span data-stu-id="63067-115">Address second line</span></span>

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

### <span data-ttu-id="63067-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="63067-116">-AddressLine3</span></span>
<span data-ttu-id="63067-117">Endereço terceira linha</span><span class="sxs-lookup"><span data-stu-id="63067-117">Address third line</span></span>

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

### <span data-ttu-id="63067-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63067-118">-AsJob</span></span>
<span data-ttu-id="63067-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="63067-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63067-120">-Cidade</span><span class="sxs-lookup"><span data-stu-id="63067-120">-City</span></span>
<span data-ttu-id="63067-121">Nome da Cidade</span><span class="sxs-lookup"><span data-stu-id="63067-121">Name of the City</span></span>

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

### <span data-ttu-id="63067-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="63067-122">-CompanyName</span></span>
<span data-ttu-id="63067-123">Nome da empresa</span><span class="sxs-lookup"><span data-stu-id="63067-123">Name of the company</span></span>

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

### <span data-ttu-id="63067-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="63067-124">-ContactPerson</span></span>
<span data-ttu-id="63067-125">Nome da pessoa de contato</span><span class="sxs-lookup"><span data-stu-id="63067-125">Name of the contact person</span></span>

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

### <span data-ttu-id="63067-126">-País/Região</span><span class="sxs-lookup"><span data-stu-id="63067-126">-Country</span></span>
<span data-ttu-id="63067-127">Nome do País</span><span class="sxs-lookup"><span data-stu-id="63067-127">Name of the Country</span></span>

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

### <span data-ttu-id="63067-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63067-128">-DefaultProfile</span></span>
<span data-ttu-id="63067-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63067-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63067-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="63067-130">-DeviceName</span></span>
<span data-ttu-id="63067-131">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="63067-131">Resource Name</span></span>

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

### <span data-ttu-id="63067-132">-Email</span><span class="sxs-lookup"><span data-stu-id="63067-132">-Email</span></span>
<span data-ttu-id="63067-133">Lista de Emails para receber atualizações, Aceita no máximo 10 emails</span><span class="sxs-lookup"><span data-stu-id="63067-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="63067-134">-Telefone</span><span class="sxs-lookup"><span data-stu-id="63067-134">-Phone</span></span>
<span data-ttu-id="63067-135">Número de telefone do contato</span><span class="sxs-lookup"><span data-stu-id="63067-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="63067-136">-Cep</span><span class="sxs-lookup"><span data-stu-id="63067-136">-PostalCode</span></span>
<span data-ttu-id="63067-137">CEP do Endereço</span><span class="sxs-lookup"><span data-stu-id="63067-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="63067-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63067-138">-ResourceGroupName</span></span>
<span data-ttu-id="63067-139">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="63067-139">Resource Group Name</span></span>

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

### <span data-ttu-id="63067-140">-Estado</span><span class="sxs-lookup"><span data-stu-id="63067-140">-State</span></span>
<span data-ttu-id="63067-141">Nome do Estado</span><span class="sxs-lookup"><span data-stu-id="63067-141">Name of the State</span></span>

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

### <span data-ttu-id="63067-142">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="63067-142">-Confirm</span></span>
<span data-ttu-id="63067-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63067-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63067-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63067-144">-WhatIf</span></span>
<span data-ttu-id="63067-145">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="63067-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63067-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="63067-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63067-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63067-147">CommonParameters</span></span>
<span data-ttu-id="63067-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63067-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63067-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63067-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63067-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="63067-150">INPUTS</span></span>

### <span data-ttu-id="63067-151">System.String</span><span class="sxs-lookup"><span data-stu-id="63067-151">System.String</span></span>

## <span data-ttu-id="63067-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="63067-152">OUTPUTS</span></span>

### <span data-ttu-id="63067-153">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="63067-153">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="63067-154">Notas</span><span class="sxs-lookup"><span data-stu-id="63067-154">NOTES</span></span>

## <span data-ttu-id="63067-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63067-155">RELATED LINKS</span></span>
