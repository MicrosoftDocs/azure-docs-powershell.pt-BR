---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: c2dc0333d2e991b21ac1a921465971f2131f5c3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432278"
---
# <span data-ttu-id="e201b-101">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e201b-101">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e201b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e201b-102">SYNOPSIS</span></span>
<span data-ttu-id="e201b-103">Exclui uma instância da capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="e201b-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e201b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e201b-104">SYNTAX</span></span>

### <span data-ttu-id="e201b-105">ByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="e201b-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e201b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e201b-106">ByResourceId</span></span>
```
Remove-AzureRmPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e201b-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e201b-107">ByInputObject</span></span>
```
Remove-AzureRmPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e201b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e201b-108">DESCRIPTION</span></span>
<span data-ttu-id="e201b-109">O cmdlet Remove-AzureRmPowerBIEmbeddedCapacity exclui uma instância da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="e201b-109">The Remove-AzureRmPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="e201b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e201b-110">EXAMPLES</span></span>

### <span data-ttu-id="e201b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e201b-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="e201b-112">Esse comando removerá a capacidade denominada testcapacity no testRG de Resource</span><span class="sxs-lookup"><span data-stu-id="e201b-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="e201b-113">OS</span><span class="sxs-lookup"><span data-stu-id="e201b-113">PARAMETERS</span></span>

### <span data-ttu-id="e201b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e201b-114">-DefaultProfile</span></span>
<span data-ttu-id="e201b-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e201b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e201b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e201b-116">-InputObject</span></span>
<span data-ttu-id="e201b-117">Objeto de entrada para tubulação</span><span class="sxs-lookup"><span data-stu-id="e201b-117">Input object for Piping</span></span>

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

### <span data-ttu-id="e201b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e201b-118">-Name</span></span>
<span data-ttu-id="e201b-119">Nome da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="e201b-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="e201b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e201b-120">-PassThru</span></span>
<span data-ttu-id="e201b-121">Retornará os detalhes de capacidade excluídos se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="e201b-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="e201b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e201b-122">-ResourceGroupName</span></span>
<span data-ttu-id="e201b-123">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="e201b-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="e201b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e201b-124">-ResourceId</span></span>
<span data-ttu-id="e201b-125">ID do recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="e201b-125">Azure resource ID</span></span>

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

### <span data-ttu-id="e201b-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e201b-126">-Confirm</span></span>
<span data-ttu-id="e201b-127">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="e201b-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="e201b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e201b-128">-WhatIf</span></span>
<span data-ttu-id="e201b-129">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="e201b-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="e201b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e201b-130">CommonParameters</span></span>
<span data-ttu-id="e201b-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e201b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e201b-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e201b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e201b-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e201b-133">INPUTS</span></span>

### <span data-ttu-id="e201b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e201b-134">System.String</span></span>

### <span data-ttu-id="e201b-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e201b-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="e201b-136">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e201b-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e201b-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e201b-137">OUTPUTS</span></span>

### <span data-ttu-id="e201b-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e201b-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e201b-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e201b-139">NOTES</span></span>

## <span data-ttu-id="e201b-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e201b-140">RELATED LINKS</span></span>

[<span data-ttu-id="e201b-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e201b-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="e201b-142">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e201b-142">New-AzureRmPowerBIEmbeddedCapacity</span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)
