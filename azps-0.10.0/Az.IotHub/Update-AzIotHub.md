---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: d1b6c8be02ee246053e5930e37186f2a7480325b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776683"
---
# <span data-ttu-id="b545a-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="b545a-101">Update-AzIotHub</span></span>

## <span data-ttu-id="b545a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b545a-102">SYNOPSIS</span></span>
<span data-ttu-id="b545a-103">Atualizar um hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="b545a-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="b545a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b545a-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b545a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b545a-105">DESCRIPTION</span></span>
<span data-ttu-id="b545a-106">Você pode atualizar as propriedades de marcas de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="b545a-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="b545a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b545a-107">EXAMPLES</span></span>

### <span data-ttu-id="b545a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b545a-108">Example 1</span></span>
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

<span data-ttu-id="b545a-109">Adicionar " @tags " à marca de um hub IOT do Azure "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="b545a-109">Add "@tags" to the Tag of an Azure IoT Hub "myiotdps".</span></span>

## <span data-ttu-id="b545a-110">OS</span><span class="sxs-lookup"><span data-stu-id="b545a-110">PARAMETERS</span></span>

### <span data-ttu-id="b545a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b545a-111">-DefaultProfile</span></span>
<span data-ttu-id="b545a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b545a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b545a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="b545a-113">-Name</span></span>
<span data-ttu-id="b545a-114">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="b545a-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b545a-115">-Redefinir</span><span class="sxs-lookup"><span data-stu-id="b545a-115">-Reset</span></span>
<span data-ttu-id="b545a-116">Redefinir as marcas IoTHub</span><span class="sxs-lookup"><span data-stu-id="b545a-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="b545a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b545a-117">-ResourceGroupName</span></span>
<span data-ttu-id="b545a-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b545a-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b545a-119">-Marca</span><span class="sxs-lookup"><span data-stu-id="b545a-119">-Tag</span></span>
<span data-ttu-id="b545a-120">Conjunto de marcas IoTHub</span><span class="sxs-lookup"><span data-stu-id="b545a-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="b545a-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b545a-121">-Confirm</span></span>
<span data-ttu-id="b545a-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b545a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b545a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b545a-123">-WhatIf</span></span>
<span data-ttu-id="b545a-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b545a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b545a-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b545a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b545a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b545a-126">CommonParameters</span></span>
<span data-ttu-id="b545a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b545a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b545a-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b545a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b545a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b545a-129">INPUTS</span></span>

### <span data-ttu-id="b545a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b545a-130">System.String</span></span>

## <span data-ttu-id="b545a-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b545a-131">OUTPUTS</span></span>

### <span data-ttu-id="b545a-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b545a-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="b545a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b545a-133">NOTES</span></span>

## <span data-ttu-id="b545a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b545a-134">RELATED LINKS</span></span>
