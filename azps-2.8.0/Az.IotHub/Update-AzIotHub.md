---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: 794ee1187043a800c6f847df215ddb288bb9da9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596227"
---
# <span data-ttu-id="d578b-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="d578b-101">Update-AzIotHub</span></span>

## <span data-ttu-id="d578b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d578b-102">SYNOPSIS</span></span>
<span data-ttu-id="d578b-103">Atualizar um hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="d578b-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="d578b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d578b-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d578b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d578b-105">DESCRIPTION</span></span>
<span data-ttu-id="d578b-106">Você pode atualizar as propriedades de marcas de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="d578b-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="d578b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d578b-107">EXAMPLES</span></span>

### <span data-ttu-id="d578b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d578b-108">Example 1</span></span>
```
PS C:\> Update-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiotdps
Name           : myiotdps
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[k1, v1]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="d578b-109">Adicionar " @tags " à marca de um hub IOT do Azure "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="d578b-109">Add "@tags" to the Tag of an Azure IoT Hub "myiotdps".</span></span>

## <span data-ttu-id="d578b-110">OS</span><span class="sxs-lookup"><span data-stu-id="d578b-110">PARAMETERS</span></span>

### <span data-ttu-id="d578b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d578b-111">-DefaultProfile</span></span>
<span data-ttu-id="d578b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d578b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d578b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d578b-113">-Name</span></span>
<span data-ttu-id="d578b-114">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="d578b-114">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d578b-115">-Redefinir</span><span class="sxs-lookup"><span data-stu-id="d578b-115">-Reset</span></span>
<span data-ttu-id="d578b-116">Redefinir as marcas IoTHub</span><span class="sxs-lookup"><span data-stu-id="d578b-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="d578b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d578b-117">-ResourceGroupName</span></span>
<span data-ttu-id="d578b-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d578b-118">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d578b-119">-Marca</span><span class="sxs-lookup"><span data-stu-id="d578b-119">-Tag</span></span>
<span data-ttu-id="d578b-120">Conjunto de marcas IoTHub</span><span class="sxs-lookup"><span data-stu-id="d578b-120">IoTHub Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d578b-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d578b-121">-Confirm</span></span>
<span data-ttu-id="d578b-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d578b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d578b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d578b-123">-WhatIf</span></span>
<span data-ttu-id="d578b-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d578b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d578b-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d578b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d578b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d578b-126">CommonParameters</span></span>
<span data-ttu-id="d578b-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d578b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d578b-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d578b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d578b-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d578b-129">INPUTS</span></span>

### <span data-ttu-id="d578b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d578b-130">System.String</span></span>

## <span data-ttu-id="d578b-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d578b-131">OUTPUTS</span></span>

### <span data-ttu-id="d578b-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d578b-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="d578b-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d578b-133">NOTES</span></span>

## <span data-ttu-id="d578b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d578b-134">RELATED LINKS</span></span>
