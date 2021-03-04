---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: b7b89f239949f6a61e3388b0f5cb794cd4ad0c53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892160"
---
# <span data-ttu-id="d6513-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="d6513-101">Update-AzIotHub</span></span>

## <span data-ttu-id="d6513-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6513-102">SYNOPSIS</span></span>
<span data-ttu-id="d6513-103">Atualize um Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="d6513-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="d6513-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d6513-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6513-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d6513-105">DESCRIPTION</span></span>
<span data-ttu-id="d6513-106">Você pode atualizar as propriedades de marcas de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="d6513-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="d6513-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6513-107">EXAMPLES</span></span>

### <span data-ttu-id="d6513-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d6513-108">Example 1</span></span>
```
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> Update-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -Tag $updatedTag

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiothub
Name           : myiothub
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[key0, value0]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="d6513-109">Atualizar marcas de um Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="d6513-109">Update tags of an IoT Hub.</span></span>

## <span data-ttu-id="d6513-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d6513-110">PARAMETERS</span></span>

### <span data-ttu-id="d6513-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6513-111">-DefaultProfile</span></span>
<span data-ttu-id="d6513-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6513-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6513-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d6513-113">-Name</span></span>
<span data-ttu-id="d6513-114">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="d6513-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d6513-115">-Reset</span><span class="sxs-lookup"><span data-stu-id="d6513-115">-Reset</span></span>
<span data-ttu-id="d6513-116">Redefinir marcas IoTHub</span><span class="sxs-lookup"><span data-stu-id="d6513-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="d6513-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6513-117">-ResourceGroupName</span></span>
<span data-ttu-id="d6513-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d6513-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d6513-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="d6513-119">-Tag</span></span>
<span data-ttu-id="d6513-120">Coleção IoTHub Tag</span><span class="sxs-lookup"><span data-stu-id="d6513-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="d6513-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6513-121">-Confirm</span></span>
<span data-ttu-id="d6513-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6513-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6513-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6513-123">-WhatIf</span></span>
<span data-ttu-id="d6513-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d6513-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6513-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6513-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6513-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6513-126">CommonParameters</span></span>
<span data-ttu-id="d6513-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6513-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6513-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6513-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6513-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6513-129">INPUTS</span></span>

### <span data-ttu-id="d6513-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d6513-130">System.String</span></span>

## <span data-ttu-id="d6513-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d6513-131">OUTPUTS</span></span>

### <span data-ttu-id="d6513-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d6513-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="d6513-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="d6513-133">NOTES</span></span>

## <span data-ttu-id="d6513-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6513-134">RELATED LINKS</span></span>
