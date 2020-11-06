---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6236a03b22bd3509933d58579db3e84d48723b68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440311"
---
# <span data-ttu-id="dc5ba-101">Update-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="dc5ba-101">Update-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="dc5ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc5ba-102">SYNOPSIS</span></span>
<span data-ttu-id="dc5ba-103">Modifica uma instância da capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="dc5ba-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc5ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc5ba-104">SYNTAX</span></span>

### <span data-ttu-id="dc5ba-105">ByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="dc5ba-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc5ba-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dc5ba-106">ByResourceId</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc5ba-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dc5ba-107">ByInputObject</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc5ba-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc5ba-108">DESCRIPTION</span></span>
<span data-ttu-id="dc5ba-109">O cmdlet Update-AzureRmPowerBIEmbeddedCapacity modifica uma instância da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="dc5ba-109">The Update-AzureRmPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="dc5ba-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc5ba-110">EXAMPLES</span></span>

### <span data-ttu-id="dc5ba-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dc5ba-111">Example 1</span></span>
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

<span data-ttu-id="dc5ba-112">Modifica a capacidade chamada testcapacity no grupo de teste de grupo de Resource para definir as marcas como key1: valor1 e Key2: value2 e administrador para testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="dc5ba-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="dc5ba-113">OS</span><span class="sxs-lookup"><span data-stu-id="dc5ba-113">PARAMETERS</span></span>

### <span data-ttu-id="dc5ba-114">-Administrador</span><span class="sxs-lookup"><span data-stu-id="dc5ba-114">-Administrator</span></span>
<span data-ttu-id="dc5ba-115">Um nome de capacidade separada por vírgulas para definir como administrador na capacidade</span><span class="sxs-lookup"><span data-stu-id="dc5ba-115">A comma separated capacity names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="dc5ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc5ba-116">-DefaultProfile</span></span>
<span data-ttu-id="dc5ba-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc5ba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc5ba-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc5ba-118">-InputObject</span></span>
<span data-ttu-id="dc5ba-119">Objeto de entrada para tubulação</span><span class="sxs-lookup"><span data-stu-id="dc5ba-119">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc5ba-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc5ba-120">-Name</span></span>
<span data-ttu-id="dc5ba-121">Nome da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="dc5ba-121">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc5ba-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc5ba-122">-PassThru</span></span>
<span data-ttu-id="dc5ba-123">Retornará os detalhes de capacidade excluídos se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="dc5ba-123">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="dc5ba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc5ba-124">-ResourceGroupName</span></span>
<span data-ttu-id="dc5ba-125">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="dc5ba-125">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc5ba-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc5ba-126">-ResourceId</span></span>
<span data-ttu-id="dc5ba-127">ResourceId da capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="dc5ba-127">PowerBI Embedded Capacity ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc5ba-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="dc5ba-128">-Sku</span></span>
<span data-ttu-id="dc5ba-129">O nome da SKU para a capacidade.</span><span class="sxs-lookup"><span data-stu-id="dc5ba-129">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc5ba-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="dc5ba-130">-Tag</span></span>
<span data-ttu-id="dc5ba-131">Pares de valores chave na forma de uma tabela de hash definidas como marcas na capacidade.</span><span class="sxs-lookup"><span data-stu-id="dc5ba-131">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc5ba-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dc5ba-132">-Confirm</span></span>
<span data-ttu-id="dc5ba-133">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="dc5ba-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="dc5ba-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc5ba-134">-WhatIf</span></span>
<span data-ttu-id="dc5ba-135">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="dc5ba-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="dc5ba-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc5ba-136">CommonParameters</span></span>
<span data-ttu-id="dc5ba-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc5ba-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc5ba-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc5ba-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc5ba-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc5ba-139">INPUTS</span></span>

### <span data-ttu-id="dc5ba-140">System. String</span><span class="sxs-lookup"><span data-stu-id="dc5ba-140">System.String</span></span>

### <span data-ttu-id="dc5ba-141">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="dc5ba-141">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="dc5ba-142">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dc5ba-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="dc5ba-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc5ba-143">OUTPUTS</span></span>

### <span data-ttu-id="dc5ba-144">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="dc5ba-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="dc5ba-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc5ba-145">NOTES</span></span>

## <span data-ttu-id="dc5ba-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc5ba-146">RELATED LINKS</span></span>

[<span data-ttu-id="dc5ba-147">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="dc5ba-147">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="dc5ba-148">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="dc5ba-148">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
