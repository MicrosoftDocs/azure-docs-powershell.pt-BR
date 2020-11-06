---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 64e96f423748e8991abcf26b178a8bd6b893cf0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426663"
---
# <span data-ttu-id="ca15d-101">Update-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="ca15d-101">Update-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="ca15d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca15d-102">SYNOPSIS</span></span>
<span data-ttu-id="ca15d-103">Modifica uma instância da capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="ca15d-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca15d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca15d-104">SYNTAX</span></span>

```
Update-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [[-Sku] <String>]
    [[-Tag] <Hashtable>] 
    [[-Administrator] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="ca15d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca15d-105">DESCRIPTION</span></span>
<span data-ttu-id="ca15d-106">O cmdlet Update-AzureRmPowerBIEmbeddedCapacity modifica uma instância da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="ca15d-106">The Update-AzureRmPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="ca15d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca15d-107">EXAMPLES</span></span>

### <span data-ttu-id="ca15d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ca15d-108">Example 1</span></span>
```
PS C:\> Update-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com, testuser2@contoso.com" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}

```

<span data-ttu-id="ca15d-109">Modifica a capacidade chamada testcapacity no grupo de teste de grupo de Resource para definir as marcas como key1: valor1 e Key2: value2 e administrador para testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="ca15d-109">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="ca15d-110">OS</span><span class="sxs-lookup"><span data-stu-id="ca15d-110">PARAMETERS</span></span>

### <span data-ttu-id="ca15d-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca15d-111">-Name</span></span>
<span data-ttu-id="ca15d-112">Nome da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="ca15d-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="ca15d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca15d-113">-ResourceGroupName</span></span>
<span data-ttu-id="ca15d-114">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="ca15d-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="ca15d-115">-SKU</span><span class="sxs-lookup"><span data-stu-id="ca15d-115">-Sku</span></span>
<span data-ttu-id="ca15d-116">O nome da SKU para a capacidade.</span><span class="sxs-lookup"><span data-stu-id="ca15d-116">The name of the Sku for the capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="ca15d-117">-Marca</span><span class="sxs-lookup"><span data-stu-id="ca15d-117">-Tag</span></span>
<span data-ttu-id="ca15d-118">Pares de valores chave na forma de uma tabela de hash definidas como marcas na capacidade.</span><span class="sxs-lookup"><span data-stu-id="ca15d-118">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```
### <span data-ttu-id="ca15d-119">-Administrador</span><span class="sxs-lookup"><span data-stu-id="ca15d-119">-Administrator</span></span>
<span data-ttu-id="ca15d-120">Um nome de capacidade separada por vírgulas para definir como administrador na capacidade</span><span class="sxs-lookup"><span data-stu-id="ca15d-120">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="ca15d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca15d-121">-ResourceId</span></span>
<span data-ttu-id="ca15d-122">ResourceId da capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="ca15d-122">PowerBI Embedded Capacity ResourceID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca15d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca15d-123">-InputObject</span></span>
<span data-ttu-id="ca15d-124">Objeto de entrada para tubulação</span><span class="sxs-lookup"><span data-stu-id="ca15d-124">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca15d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca15d-125">-PassThru</span></span>
<span data-ttu-id="ca15d-126">Retornará os detalhes de capacidade excluídos se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="ca15d-126">Will return the deleted capacity details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca15d-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ca15d-127">-Confirm</span></span>
<span data-ttu-id="ca15d-128">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="ca15d-128">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca15d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca15d-129">-WhatIf</span></span>
<span data-ttu-id="ca15d-130">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="ca15d-130">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca15d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca15d-131">CommonParameters</span></span>
<span data-ttu-id="ca15d-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca15d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca15d-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca15d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca15d-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca15d-134">INPUTS</span></span>

### <span data-ttu-id="ca15d-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ca15d-135">None</span></span>
<span data-ttu-id="ca15d-136">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ca15d-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ca15d-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca15d-137">OUTPUTS</span></span>

### <span data-ttu-id="ca15d-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="ca15d-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="ca15d-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca15d-139">NOTES</span></span>

## <span data-ttu-id="ca15d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca15d-140">RELATED LINKS</span></span>

[<span data-ttu-id="ca15d-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="ca15d-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="ca15d-142">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="ca15d-142">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
