---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 5a9dc29d9cb078473a777279c5bdb648a1b9388e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433673"
---
# <span data-ttu-id="942e4-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="942e4-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="942e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="942e4-102">SYNOPSIS</span></span>
<span data-ttu-id="942e4-103">Exclui um aplicativo da central de IoT.</span><span class="sxs-lookup"><span data-stu-id="942e4-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="942e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="942e4-104">SYNTAX</span></span>

### <span data-ttu-id="942e4-105">ResourceIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="942e4-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="942e4-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="942e4-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="942e4-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="942e4-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="942e4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="942e4-108">DESCRIPTION</span></span>
<span data-ttu-id="942e4-109">Exclui um aplicativo Central do IoT existente.</span><span class="sxs-lookup"><span data-stu-id="942e4-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="942e4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="942e4-110">EXAMPLES</span></span>

### <span data-ttu-id="942e4-111">Exemplo 1-excluir e aplicativo Central de IoT</span><span class="sxs-lookup"><span data-stu-id="942e4-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="942e4-112">Exclui o aplicativo da central de IoT fornecido.</span><span class="sxs-lookup"><span data-stu-id="942e4-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="942e4-113">OS</span><span class="sxs-lookup"><span data-stu-id="942e4-113">PARAMETERS</span></span>

### <span data-ttu-id="942e4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="942e4-114">-AsJob</span></span>
<span data-ttu-id="942e4-115">Executar o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="942e4-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="942e4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="942e4-116">-DefaultProfile</span></span>
<span data-ttu-id="942e4-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="942e4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="942e4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="942e4-118">-InputObject</span></span>
<span data-ttu-id="942e4-119">Objeto de entrada de aplicativo do IOT central.</span><span class="sxs-lookup"><span data-stu-id="942e4-119">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="942e4-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="942e4-120">-Name</span></span>
<span data-ttu-id="942e4-121">Nome do recurso de aplicativo da central do IOT.</span><span class="sxs-lookup"><span data-stu-id="942e4-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="942e4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="942e4-122">-PassThru</span></span>
<span data-ttu-id="942e4-123">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="942e4-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="942e4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="942e4-124">-ResourceGroupName</span></span>
<span data-ttu-id="942e4-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="942e4-125">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="942e4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="942e4-126">-ResourceId</span></span>
<span data-ttu-id="942e4-127">ID do recurso de aplicativo do IOT central.</span><span class="sxs-lookup"><span data-stu-id="942e4-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="942e4-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="942e4-128">-Confirm</span></span>
<span data-ttu-id="942e4-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="942e4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="942e4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="942e4-130">-WhatIf</span></span>
<span data-ttu-id="942e4-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="942e4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="942e4-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="942e4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="942e4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="942e4-133">CommonParameters</span></span>
<span data-ttu-id="942e4-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="942e4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="942e4-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="942e4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="942e4-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="942e4-136">INPUTS</span></span>

### <span data-ttu-id="942e4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="942e4-137">System.String</span></span>

### <span data-ttu-id="942e4-138">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="942e4-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="942e4-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="942e4-139">OUTPUTS</span></span>

### <span data-ttu-id="942e4-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="942e4-140">System.Boolean</span></span>

## <span data-ttu-id="942e4-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="942e4-141">NOTES</span></span>

## <span data-ttu-id="942e4-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="942e4-142">RELATED LINKS</span></span>
