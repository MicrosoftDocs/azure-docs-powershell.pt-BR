---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: fce61fd015271c9f6b5a3752fae33eaa80d6447c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113116"
---
# <span data-ttu-id="dd8ce-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="dd8ce-101">Update-AzIotHub</span></span>

## <span data-ttu-id="dd8ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd8ce-102">SYNOPSIS</span></span>
<span data-ttu-id="dd8ce-103">Atualizar um Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="dd8ce-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="dd8ce-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd8ce-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd8ce-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd8ce-105">DESCRIPTION</span></span>
<span data-ttu-id="dd8ce-106">Você pode atualizar as propriedades de marcas de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="dd8ce-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="dd8ce-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dd8ce-107">EXAMPLES</span></span>

### <span data-ttu-id="dd8ce-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dd8ce-108">Example 1</span></span>
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

<span data-ttu-id="dd8ce-109">Atualizar marcas de um Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="dd8ce-109">Update tags of an IoT Hub.</span></span>

## <span data-ttu-id="dd8ce-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd8ce-110">PARAMETERS</span></span>

### <span data-ttu-id="dd8ce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd8ce-111">-DefaultProfile</span></span>
<span data-ttu-id="dd8ce-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd8ce-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd8ce-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd8ce-113">-Name</span></span>
<span data-ttu-id="dd8ce-114">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="dd8ce-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="dd8ce-115">-Redefinir</span><span class="sxs-lookup"><span data-stu-id="dd8ce-115">-Reset</span></span>
<span data-ttu-id="dd8ce-116">Redefinir marcas do IoTHub</span><span class="sxs-lookup"><span data-stu-id="dd8ce-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="dd8ce-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd8ce-117">-ResourceGroupName</span></span>
<span data-ttu-id="dd8ce-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="dd8ce-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dd8ce-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="dd8ce-119">-Tag</span></span>
<span data-ttu-id="dd8ce-120">Coleção de marca do IoTHub</span><span class="sxs-lookup"><span data-stu-id="dd8ce-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="dd8ce-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="dd8ce-121">-Confirm</span></span>
<span data-ttu-id="dd8ce-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd8ce-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd8ce-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd8ce-123">-WhatIf</span></span>
<span data-ttu-id="dd8ce-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="dd8ce-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd8ce-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dd8ce-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd8ce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd8ce-126">CommonParameters</span></span>
<span data-ttu-id="dd8ce-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd8ce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd8ce-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd8ce-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd8ce-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="dd8ce-129">INPUTS</span></span>

### <span data-ttu-id="dd8ce-130">System.String</span><span class="sxs-lookup"><span data-stu-id="dd8ce-130">System.String</span></span>

## <span data-ttu-id="dd8ce-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="dd8ce-131">OUTPUTS</span></span>

### <span data-ttu-id="dd8ce-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dd8ce-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="dd8ce-133">Notas</span><span class="sxs-lookup"><span data-stu-id="dd8ce-133">NOTES</span></span>

## <span data-ttu-id="dd8ce-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd8ce-134">RELATED LINKS</span></span>
