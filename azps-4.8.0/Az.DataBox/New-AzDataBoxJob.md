---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 4402eaed4b76ce6e769141748b043598bdfd099a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114595"
---
# <span data-ttu-id="4dd53-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="4dd53-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="4dd53-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4dd53-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd53-103">Cria um novo trabalho do databox usando os parâmetros especificados</span><span class="sxs-lookup"><span data-stu-id="4dd53-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="4dd53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4dd53-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dd53-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4dd53-105">DESCRIPTION</span></span>
<span data-ttu-id="4dd53-106">O cmdlet **New-AzDataBoxJob** é usado para criar um novo trabalho do databox especificando os detalhes necessários para a criação do trabalho.</span><span class="sxs-lookup"><span data-stu-id="4dd53-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="4dd53-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4dd53-107">EXAMPLES</span></span>

### <span data-ttu-id="4dd53-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4dd53-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="4dd53-109">O cmdlet assume todos os parâmetros necessários e alguns parâmetros opcionais para criar o trabalho databox.</span><span class="sxs-lookup"><span data-stu-id="4dd53-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="4dd53-110">OS</span><span class="sxs-lookup"><span data-stu-id="4dd53-110">PARAMETERS</span></span>

### <span data-ttu-id="4dd53-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="4dd53-111">-AddressType</span></span>
<span data-ttu-id="4dd53-112">Tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="4dd53-112">Type of Address.</span></span> <span data-ttu-id="4dd53-113">Valores disponíveis: AddressType. None (padrão), AddressType. residencial, AddressType. Commercial</span><span class="sxs-lookup"><span data-stu-id="4dd53-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

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

### <span data-ttu-id="4dd53-114">-Cidade</span><span class="sxs-lookup"><span data-stu-id="4dd53-114">-City</span></span>
<span data-ttu-id="4dd53-115">Nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="4dd53-115">Name of the City.</span></span> <span data-ttu-id="4dd53-116">Por exemplo: San Francisco</span><span class="sxs-lookup"><span data-stu-id="4dd53-116">Ex : San Francisco</span></span>

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

### <span data-ttu-id="4dd53-117">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="4dd53-117">-CompanyName</span></span>
<span data-ttu-id="4dd53-118">Nome da empresa</span><span class="sxs-lookup"><span data-stu-id="4dd53-118">Name of the company</span></span>

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

### <span data-ttu-id="4dd53-119">-ContactName</span><span class="sxs-lookup"><span data-stu-id="4dd53-119">-ContactName</span></span>
<span data-ttu-id="4dd53-120">Nome do contato</span><span class="sxs-lookup"><span data-stu-id="4dd53-120">Contact Name</span></span>

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

### <span data-ttu-id="4dd53-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="4dd53-121">-CountryCode</span></span>
<span data-ttu-id="4dd53-122">Código do país.</span><span class="sxs-lookup"><span data-stu-id="4dd53-122">Country Code.</span></span> <span data-ttu-id="4dd53-123">Exemplo: EUA</span><span class="sxs-lookup"><span data-stu-id="4dd53-123">Ex: US</span></span>

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

### <span data-ttu-id="4dd53-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="4dd53-124">-DataBoxType</span></span>
<span data-ttu-id="4dd53-125">Tipo de SKU do Databox.</span><span class="sxs-lookup"><span data-stu-id="4dd53-125">Sku type of Databox.</span></span>  <span data-ttu-id="4dd53-126">Valores disponíveis: DataBoxDisk, Databox, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="4dd53-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

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

### <span data-ttu-id="4dd53-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd53-127">-DefaultProfile</span></span>
<span data-ttu-id="4dd53-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd53-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dd53-129">-Emailid</span><span class="sxs-lookup"><span data-stu-id="4dd53-129">-EmailId</span></span>
<span data-ttu-id="4dd53-130">A lista de EmailIds pode ser fornecida.</span><span class="sxs-lookup"><span data-stu-id="4dd53-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="4dd53-131">Pelo menos um é obrigatório</span><span class="sxs-lookup"><span data-stu-id="4dd53-131">Atleast one is mandatory</span></span>

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

### <span data-ttu-id="4dd53-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="4dd53-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="4dd53-133">Para o pedido DataBoxDisk, especificar os dados esperados em terabytes é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4dd53-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

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

### <span data-ttu-id="4dd53-134">-Local</span><span class="sxs-lookup"><span data-stu-id="4dd53-134">-Location</span></span>
<span data-ttu-id="4dd53-135">Localização da assinatura</span><span class="sxs-lookup"><span data-stu-id="4dd53-135">Location of the subscription</span></span>

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

### <span data-ttu-id="4dd53-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="4dd53-136">-Name</span></span>
<span data-ttu-id="4dd53-137">Nome do trabalho de databox a ser criado</span><span class="sxs-lookup"><span data-stu-id="4dd53-137">Name of the databox job to be created</span></span>

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

### <span data-ttu-id="4dd53-138">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="4dd53-138">-PhoneNumber</span></span>
<span data-ttu-id="4dd53-139">Número de contato</span><span class="sxs-lookup"><span data-stu-id="4dd53-139">Contact Number</span></span> 

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

### <span data-ttu-id="4dd53-140">-CEP</span><span class="sxs-lookup"><span data-stu-id="4dd53-140">-PostalCode</span></span>
<span data-ttu-id="4dd53-141">Código postal</span><span class="sxs-lookup"><span data-stu-id="4dd53-141">Postal Code</span></span>

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

### <span data-ttu-id="4dd53-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dd53-142">-ResourceGroupName</span></span>
<span data-ttu-id="4dd53-143">Nome do grupo de recursos sob o qual o trabalho de databox deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="4dd53-143">Resource Group Name under which the databox job has to be created.</span></span>

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

### <span data-ttu-id="4dd53-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="4dd53-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="4dd53-145">Insira o código do Estado ou província.</span><span class="sxs-lookup"><span data-stu-id="4dd53-145">Input the state or province code.</span></span> <span data-ttu-id="4dd53-146">Como CA-Califórnia; FL-Flórida; NY-Nova York</span><span class="sxs-lookup"><span data-stu-id="4dd53-146">Like CA - California; FL - Florida; NY - New York</span></span>

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

### <span data-ttu-id="4dd53-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="4dd53-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="4dd53-148">Lista de IDs de recursos das contas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4dd53-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="4dd53-149">Pelo menos um é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4dd53-149">Atleast one is mandatory.</span></span>

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

### <span data-ttu-id="4dd53-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="4dd53-150">-StreetAddress1</span></span>
<span data-ttu-id="4dd53-151">Endereço da rua</span><span class="sxs-lookup"><span data-stu-id="4dd53-151">Street Address</span></span>

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

### <span data-ttu-id="4dd53-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="4dd53-152">-StreetAddress2</span></span>
<span data-ttu-id="4dd53-153">Endereço adicional</span><span class="sxs-lookup"><span data-stu-id="4dd53-153">Additional Street Address</span></span>

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

### <span data-ttu-id="4dd53-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="4dd53-154">-StreetAddress3</span></span>
<span data-ttu-id="4dd53-155">Endereço adicional</span><span class="sxs-lookup"><span data-stu-id="4dd53-155">Additional Street Address</span></span>

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

### <span data-ttu-id="4dd53-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4dd53-156">-Confirm</span></span>
<span data-ttu-id="4dd53-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dd53-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dd53-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dd53-158">-WhatIf</span></span>
<span data-ttu-id="4dd53-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4dd53-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4dd53-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4dd53-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dd53-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd53-161">CommonParameters</span></span>
<span data-ttu-id="4dd53-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dd53-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd53-163">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4dd53-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd53-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4dd53-164">INPUTS</span></span>

### <span data-ttu-id="4dd53-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="4dd53-165">System.String[]</span></span>

## <span data-ttu-id="4dd53-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4dd53-166">OUTPUTS</span></span>

### <span data-ttu-id="4dd53-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="4dd53-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="4dd53-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4dd53-168">NOTES</span></span>

## <span data-ttu-id="4dd53-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4dd53-169">RELATED LINKS</span></span>
