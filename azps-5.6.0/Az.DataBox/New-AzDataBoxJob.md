---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 2c78f8b40621ba58b84169f2bd9022399fce80b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891476"
---
# <span data-ttu-id="aefdd-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="aefdd-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="aefdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aefdd-102">SYNOPSIS</span></span>
<span data-ttu-id="aefdd-103">Cria um novo trabalho de caixa de dados usando os parâmetros especificados</span><span class="sxs-lookup"><span data-stu-id="aefdd-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="aefdd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aefdd-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aefdd-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aefdd-105">DESCRIPTION</span></span>
<span data-ttu-id="aefdd-106">O cmdlet **New-AzDataBoxJob** é usado para criar um novo trabalho de caixa de dados especificando os detalhes necessários para a criação do trabalho.</span><span class="sxs-lookup"><span data-stu-id="aefdd-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="aefdd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aefdd-107">EXAMPLES</span></span>

### <span data-ttu-id="aefdd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aefdd-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="aefdd-109">O cmdlet aceita todos os parâmetros necessários e alguns parâmetros opcionais para criar o trabalho da caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="aefdd-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="aefdd-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aefdd-110">PARAMETERS</span></span>

### <span data-ttu-id="aefdd-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="aefdd-111">-AddressType</span></span>
<span data-ttu-id="aefdd-112">Tipo de Endereço.</span><span class="sxs-lookup"><span data-stu-id="aefdd-112">Type of Address.</span></span> <span data-ttu-id="aefdd-113">Valores disponíveis: AddressType.None (padrão), AddressType.Residential, AddressType.Commercial</span><span class="sxs-lookup"><span data-stu-id="aefdd-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

```yaml
Type: Microsoft.Azure.Management.DataBox.Models.AddressType
Parameter Sets: (All)
Aliases:
Accepted values: None, Residential, Commercial

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefdd-114">-City</span><span class="sxs-lookup"><span data-stu-id="aefdd-114">-City</span></span>
<span data-ttu-id="aefdd-115">Nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="aefdd-115">Name of the City.</span></span> <span data-ttu-id="aefdd-116">Ex : São Francisco</span><span class="sxs-lookup"><span data-stu-id="aefdd-116">Ex : San Francisco</span></span>

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

### <span data-ttu-id="aefdd-117">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="aefdd-117">-CompanyName</span></span>
<span data-ttu-id="aefdd-118">Nome da empresa</span><span class="sxs-lookup"><span data-stu-id="aefdd-118">Name of the company</span></span>

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

### <span data-ttu-id="aefdd-119">-ContactName</span><span class="sxs-lookup"><span data-stu-id="aefdd-119">-ContactName</span></span>
<span data-ttu-id="aefdd-120">Nome do contato</span><span class="sxs-lookup"><span data-stu-id="aefdd-120">Contact Name</span></span>

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

### <span data-ttu-id="aefdd-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="aefdd-121">-CountryCode</span></span>
<span data-ttu-id="aefdd-122">Código do País.</span><span class="sxs-lookup"><span data-stu-id="aefdd-122">Country Code.</span></span> <span data-ttu-id="aefdd-123">Ex: US</span><span class="sxs-lookup"><span data-stu-id="aefdd-123">Ex: US</span></span>

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

### <span data-ttu-id="aefdd-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="aefdd-124">-DataBoxType</span></span>
<span data-ttu-id="aefdd-125">Tipo Sku de Databox.</span><span class="sxs-lookup"><span data-stu-id="aefdd-125">Sku type of Databox.</span></span>  <span data-ttu-id="aefdd-126">Valores disponíveis : DataBoxDisk, Databox, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="aefdd-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DataBoxDisk, Databox, DataBoxHeavy

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefdd-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aefdd-127">-DefaultProfile</span></span>
<span data-ttu-id="aefdd-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aefdd-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aefdd-129">-EmailId</span><span class="sxs-lookup"><span data-stu-id="aefdd-129">-EmailId</span></span>
<span data-ttu-id="aefdd-130">A lista de EmailIds pode ser fornecida.</span><span class="sxs-lookup"><span data-stu-id="aefdd-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="aefdd-131">Pelo menos um é obrigatório</span><span class="sxs-lookup"><span data-stu-id="aefdd-131">Atleast one is mandatory</span></span>

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

### <span data-ttu-id="aefdd-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="aefdd-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="aefdd-133">Para a ordem DataBoxDisk, a especificação dos dados esperados em terabytes é obrigatória.</span><span class="sxs-lookup"><span data-stu-id="aefdd-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefdd-134">-Location</span><span class="sxs-lookup"><span data-stu-id="aefdd-134">-Location</span></span>
<span data-ttu-id="aefdd-135">Local da assinatura</span><span class="sxs-lookup"><span data-stu-id="aefdd-135">Location of the subscription</span></span>

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

### <span data-ttu-id="aefdd-136">-Name</span><span class="sxs-lookup"><span data-stu-id="aefdd-136">-Name</span></span>
<span data-ttu-id="aefdd-137">Nome do trabalho de caixa de dados a ser criado</span><span class="sxs-lookup"><span data-stu-id="aefdd-137">Name of the databox job to be created</span></span>

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

### <span data-ttu-id="aefdd-138">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="aefdd-138">-PhoneNumber</span></span>
<span data-ttu-id="aefdd-139">Número de contato</span><span class="sxs-lookup"><span data-stu-id="aefdd-139">Contact Number</span></span> 

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

### <span data-ttu-id="aefdd-140">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="aefdd-140">-PostalCode</span></span>
<span data-ttu-id="aefdd-141">Código Postal</span><span class="sxs-lookup"><span data-stu-id="aefdd-141">Postal Code</span></span>

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

### <span data-ttu-id="aefdd-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aefdd-142">-ResourceGroupName</span></span>
<span data-ttu-id="aefdd-143">Nome do Grupo de Recursos sob o qual o trabalho da caixa de dados deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="aefdd-143">Resource Group Name under which the databox job has to be created.</span></span>

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

### <span data-ttu-id="aefdd-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="aefdd-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="aefdd-145">Input the state or province code.</span><span class="sxs-lookup"><span data-stu-id="aefdd-145">Input the state or province code.</span></span> <span data-ttu-id="aefdd-146">Como CA - Califórnia; FL - Flórida; NY - Nova York</span><span class="sxs-lookup"><span data-stu-id="aefdd-146">Like CA - California; FL - Florida; NY - New York</span></span>

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

### <span data-ttu-id="aefdd-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="aefdd-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="aefdd-148">Lista de IDs de Recursos de Contas de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="aefdd-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="aefdd-149">Pelo menos um é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="aefdd-149">Atleast one is mandatory.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aefdd-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="aefdd-150">-StreetAddress1</span></span>
<span data-ttu-id="aefdd-151">Endereço de rua</span><span class="sxs-lookup"><span data-stu-id="aefdd-151">Street Address</span></span>

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

### <span data-ttu-id="aefdd-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="aefdd-152">-StreetAddress2</span></span>
<span data-ttu-id="aefdd-153">Endereço de rua adicional</span><span class="sxs-lookup"><span data-stu-id="aefdd-153">Additional Street Address</span></span>

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

### <span data-ttu-id="aefdd-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="aefdd-154">-StreetAddress3</span></span>
<span data-ttu-id="aefdd-155">Endereço de rua adicional</span><span class="sxs-lookup"><span data-stu-id="aefdd-155">Additional Street Address</span></span>

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

### <span data-ttu-id="aefdd-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aefdd-156">-Confirm</span></span>
<span data-ttu-id="aefdd-157">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aefdd-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aefdd-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aefdd-158">-WhatIf</span></span>
<span data-ttu-id="aefdd-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aefdd-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aefdd-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aefdd-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aefdd-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aefdd-161">CommonParameters</span></span>
<span data-ttu-id="aefdd-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aefdd-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aefdd-163">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aefdd-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aefdd-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aefdd-164">INPUTS</span></span>

### <span data-ttu-id="aefdd-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="aefdd-165">System.String[]</span></span>

## <span data-ttu-id="aefdd-166">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aefdd-166">OUTPUTS</span></span>

### <span data-ttu-id="aefdd-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="aefdd-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="aefdd-168">NOTES</span><span class="sxs-lookup"><span data-stu-id="aefdd-168">NOTES</span></span>

## <span data-ttu-id="aefdd-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aefdd-169">RELATED LINKS</span></span>
