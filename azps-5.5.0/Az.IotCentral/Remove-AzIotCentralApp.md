---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 5a9dc29d9cb078473a777279c5bdb648a1b9388e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113627"
---
# <span data-ttu-id="a175e-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="a175e-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="a175e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a175e-102">SYNOPSIS</span></span>
<span data-ttu-id="a175e-103">Exclui um Aplicativo Central de IoT.</span><span class="sxs-lookup"><span data-stu-id="a175e-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="a175e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a175e-104">SYNTAX</span></span>

### <span data-ttu-id="a175e-105">ResourceIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a175e-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a175e-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a175e-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a175e-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="a175e-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a175e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a175e-108">DESCRIPTION</span></span>
<span data-ttu-id="a175e-109">Exclui um Aplicativo Central de IoT existente.</span><span class="sxs-lookup"><span data-stu-id="a175e-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="a175e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a175e-110">EXAMPLES</span></span>

### <span data-ttu-id="a175e-111">Exemplo 1 Excluir e IoT Aplicativo Central</span><span class="sxs-lookup"><span data-stu-id="a175e-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="a175e-112">Exclui o Aplicativo Central de IoT fornecido.</span><span class="sxs-lookup"><span data-stu-id="a175e-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="a175e-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a175e-113">PARAMETERS</span></span>

### <span data-ttu-id="a175e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a175e-114">-AsJob</span></span>
<span data-ttu-id="a175e-115">Execute o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="a175e-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="a175e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a175e-116">-DefaultProfile</span></span>
<span data-ttu-id="a175e-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a175e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a175e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a175e-118">-InputObject</span></span>
<span data-ttu-id="a175e-119">Iot Central Application Input Object.</span><span class="sxs-lookup"><span data-stu-id="a175e-119">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="a175e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a175e-120">-Name</span></span>
<span data-ttu-id="a175e-121">Nome do Recurso de Aplicativo Central de Iot.</span><span class="sxs-lookup"><span data-stu-id="a175e-121">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="a175e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a175e-122">-PassThru</span></span>
<span data-ttu-id="a175e-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a175e-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a175e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a175e-124">-ResourceGroupName</span></span>
<span data-ttu-id="a175e-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="a175e-125">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="a175e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a175e-126">-ResourceId</span></span>
<span data-ttu-id="a175e-127">Iot Central Application Resource Id.</span><span class="sxs-lookup"><span data-stu-id="a175e-127">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="a175e-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a175e-128">-Confirm</span></span>
<span data-ttu-id="a175e-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a175e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a175e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a175e-130">-WhatIf</span></span>
<span data-ttu-id="a175e-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a175e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a175e-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a175e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a175e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a175e-133">CommonParameters</span></span>
<span data-ttu-id="a175e-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a175e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a175e-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a175e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a175e-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="a175e-136">INPUTS</span></span>

### <span data-ttu-id="a175e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a175e-137">System.String</span></span>

### <span data-ttu-id="a175e-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="a175e-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="a175e-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="a175e-139">OUTPUTS</span></span>

### <span data-ttu-id="a175e-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a175e-140">System.Boolean</span></span>

## <span data-ttu-id="a175e-141">Notas</span><span class="sxs-lookup"><span data-stu-id="a175e-141">NOTES</span></span>

## <span data-ttu-id="a175e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a175e-142">RELATED LINKS</span></span>
