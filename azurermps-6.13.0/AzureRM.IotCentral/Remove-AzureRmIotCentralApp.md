---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/remove-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Remove-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Remove-AzureRmIotCentralApp.md
ms.openlocfilehash: c8a2f32b82a6111c1117a4134f0f7fe8b96a966f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441271"
---
# <span data-ttu-id="fa2d6-101">Remove-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="fa2d6-101">Remove-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="fa2d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa2d6-102">SYNOPSIS</span></span>
<span data-ttu-id="fa2d6-103">Exclui um aplicativo da central de IoT.</span><span class="sxs-lookup"><span data-stu-id="fa2d6-103">Deletes an IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa2d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa2d6-104">SYNTAX</span></span>

### <span data-ttu-id="fa2d6-105">ResourceIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fa2d6-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa2d6-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa2d6-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa2d6-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa2d6-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa2d6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa2d6-108">DESCRIPTION</span></span>
<span data-ttu-id="fa2d6-109">Exclui um aplicativo Central do IoT existente.</span><span class="sxs-lookup"><span data-stu-id="fa2d6-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="fa2d6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa2d6-110">EXAMPLES</span></span>

### <span data-ttu-id="fa2d6-111">Exemplo 1-excluir e aplicativo Central de IoT</span><span class="sxs-lookup"><span data-stu-id="fa2d6-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="fa2d6-112">Exclui o aplicativo da central de IoT fornecido.</span><span class="sxs-lookup"><span data-stu-id="fa2d6-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="fa2d6-113">OS</span><span class="sxs-lookup"><span data-stu-id="fa2d6-113">PARAMETERS</span></span>

### <span data-ttu-id="fa2d6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa2d6-114">-AsJob</span></span>
<span data-ttu-id="fa2d6-115">Executar o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="fa2d6-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="fa2d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa2d6-116">-DefaultProfile</span></span>
<span data-ttu-id="fa2d6-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fa2d6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2d6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa2d6-118">-InputObject</span></span>
<span data-ttu-id="fa2d6-119">Objeto de entrada de aplicativo do IOT central.</span><span class="sxs-lookup"><span data-stu-id="fa2d6-119">Iot Central Application Input Object.</span></span>

```yaml
Type: PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa2d6-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa2d6-120">-Name</span></span>
<span data-ttu-id="fa2d6-121">Nome do recurso de aplicativo da central do IOT.</span><span class="sxs-lookup"><span data-stu-id="fa2d6-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2d6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa2d6-122">-PassThru</span></span>
<span data-ttu-id="fa2d6-123">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="fa2d6-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fa2d6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa2d6-124">-ResourceGroupName</span></span>
<span data-ttu-id="fa2d6-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fa2d6-125">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2d6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa2d6-126">-ResourceId</span></span>
<span data-ttu-id="fa2d6-127">ID do recurso de aplicativo do IOT central.</span><span class="sxs-lookup"><span data-stu-id="fa2d6-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa2d6-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fa2d6-128">-Confirm</span></span>
<span data-ttu-id="fa2d6-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa2d6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa2d6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa2d6-130">-WhatIf</span></span>
<span data-ttu-id="fa2d6-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fa2d6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa2d6-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fa2d6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa2d6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa2d6-133">CommonParameters</span></span>
<span data-ttu-id="fa2d6-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa2d6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa2d6-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa2d6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa2d6-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa2d6-136">INPUTS</span></span>

### <span data-ttu-id="fa2d6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fa2d6-137">System.String</span></span>
### <span data-ttu-id="fa2d6-138">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="fa2d6-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="fa2d6-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa2d6-139">OUTPUTS</span></span>

### <span data-ttu-id="fa2d6-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa2d6-140">System.Boolean</span></span>
## <span data-ttu-id="fa2d6-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa2d6-141">NOTES</span></span>

## <span data-ttu-id="fa2d6-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa2d6-142">RELATED LINKS</span></span>
