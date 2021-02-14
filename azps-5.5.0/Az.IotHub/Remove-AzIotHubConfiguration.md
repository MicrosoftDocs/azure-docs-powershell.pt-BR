---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
ms.openlocfilehash: 0b87bece7bca0ea3f534746dd20a163f69f21262
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116734"
---
# <span data-ttu-id="b131a-101">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="b131a-101">Remove-AzIotHubConfiguration</span></span>

## <span data-ttu-id="b131a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b131a-102">SYNOPSIS</span></span>
<span data-ttu-id="b131a-103">Exclua uma configuração de dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="b131a-103">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="b131a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b131a-104">SYNTAX</span></span>

### <span data-ttu-id="b131a-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b131a-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b131a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b131a-106">InputObjectSet</span></span>
```
Remove-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b131a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b131a-107">ResourceIdSet</span></span>
```
Remove-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b131a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b131a-108">DESCRIPTION</span></span>
<span data-ttu-id="b131a-109">Confira https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management mais informações.</span><span class="sxs-lookup"><span data-stu-id="b131a-109">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="b131a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b131a-110">EXAMPLES</span></span>

### <span data-ttu-id="b131a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b131a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="b131a-112">Exclua uma configuração de dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="b131a-112">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="b131a-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b131a-113">PARAMETERS</span></span>

### <span data-ttu-id="b131a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b131a-114">-DefaultProfile</span></span>
<span data-ttu-id="b131a-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b131a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b131a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b131a-116">-InputObject</span></span>
<span data-ttu-id="b131a-117">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="b131a-117">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b131a-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b131a-118">-IotHubName</span></span>
<span data-ttu-id="b131a-119">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="b131a-119">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b131a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b131a-120">-Name</span></span>
<span data-ttu-id="b131a-121">Identificador da configuração.</span><span class="sxs-lookup"><span data-stu-id="b131a-121">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="b131a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b131a-122">-PassThru</span></span>
<span data-ttu-id="b131a-123">Permite retornar o objeto boolano.</span><span class="sxs-lookup"><span data-stu-id="b131a-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="b131a-124">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="b131a-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b131a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b131a-125">-ResourceGroupName</span></span>
<span data-ttu-id="b131a-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="b131a-126">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b131a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b131a-127">-ResourceId</span></span>
<span data-ttu-id="b131a-128">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="b131a-128">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b131a-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b131a-129">-Confirm</span></span>
<span data-ttu-id="b131a-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b131a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b131a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b131a-131">-WhatIf</span></span>
<span data-ttu-id="b131a-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b131a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b131a-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b131a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b131a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b131a-134">CommonParameters</span></span>
<span data-ttu-id="b131a-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b131a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b131a-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b131a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b131a-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="b131a-137">INPUTS</span></span>

### <span data-ttu-id="b131a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b131a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b131a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b131a-139">System.String</span></span>

## <span data-ttu-id="b131a-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="b131a-140">OUTPUTS</span></span>

### <span data-ttu-id="b131a-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b131a-141">System.Boolean</span></span>

## <span data-ttu-id="b131a-142">Notas</span><span class="sxs-lookup"><span data-stu-id="b131a-142">NOTES</span></span>

## <span data-ttu-id="b131a-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b131a-143">RELATED LINKS</span></span>
