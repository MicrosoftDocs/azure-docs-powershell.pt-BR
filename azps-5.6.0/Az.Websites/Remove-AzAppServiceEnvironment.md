---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServiceEnvironment.md
ms.openlocfilehash: 73c7a7b76f882678612eb6f2a1fb682637705858
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887646"
---
# <span data-ttu-id="61929-101">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="61929-101">Remove-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="61929-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61929-102">SYNOPSIS</span></span>
<span data-ttu-id="61929-103">Remover ambiente de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="61929-103">Remove App Service Environment.</span></span>

## <span data-ttu-id="61929-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="61929-104">SYNTAX</span></span>

### <span data-ttu-id="61929-105">InputValuesParameterSet</span><span class="sxs-lookup"><span data-stu-id="61929-105">InputValuesParameterSet</span></span>
```
Remove-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61929-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61929-106">InputObjectParameterSet</span></span>
```
Remove-AzAppServiceEnvironment [-Force] [-PassThru] [-AsJob] -InputObject <PSAppServiceEnvironment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61929-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="61929-107">DESCRIPTION</span></span>
<span data-ttu-id="61929-108">O cmdlet **Remove-AzAppServiceEnvironment** remove um Ambiente de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="61929-108">The **Remove-AzAppServiceEnvironment** cmdlet removes an App Service Environment.</span></span> <span data-ttu-id="61929-109">Qualquer Plano de Serviço de Aplicativo deve ser excluído antes de excluir o ASE.</span><span class="sxs-lookup"><span data-stu-id="61929-109">Any App Service Plan must be deleted prior to deleting the ASE.</span></span>

## <span data-ttu-id="61929-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61929-110">EXAMPLES</span></span>

### <span data-ttu-id="61929-111">Exemplo 1 : Excluir um ambiente de serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="61929-111">Example 1 : Delete an App Service Environment</span></span>
```powershell
PS C:\> Remove-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseName
```

<span data-ttu-id="61929-112">Excluir um ambiente de serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="61929-112">Delete an App Service Environment</span></span>

## <span data-ttu-id="61929-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="61929-113">PARAMETERS</span></span>

### <span data-ttu-id="61929-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61929-114">-AsJob</span></span>
<span data-ttu-id="61929-115">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="61929-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="61929-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61929-116">-DefaultProfile</span></span>
<span data-ttu-id="61929-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61929-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61929-118">-Force</span><span class="sxs-lookup"><span data-stu-id="61929-118">-Force</span></span>
<span data-ttu-id="61929-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="61929-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="61929-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61929-120">-InputObject</span></span>
<span data-ttu-id="61929-121">O objeto do ambiente de serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="61929-121">The app service environment object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61929-122">-Name</span><span class="sxs-lookup"><span data-stu-id="61929-122">-Name</span></span>
<span data-ttu-id="61929-123">O nome do ambiente de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="61929-123">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61929-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61929-124">-PassThru</span></span>
<span data-ttu-id="61929-125">Status de retorno.</span><span class="sxs-lookup"><span data-stu-id="61929-125">Return status.</span></span>

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

### <span data-ttu-id="61929-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61929-126">-ResourceGroupName</span></span>
<span data-ttu-id="61929-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="61929-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61929-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61929-128">-Confirm</span></span>
<span data-ttu-id="61929-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61929-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61929-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61929-130">-WhatIf</span></span>
<span data-ttu-id="61929-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="61929-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61929-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="61929-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61929-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61929-133">CommonParameters</span></span>
<span data-ttu-id="61929-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61929-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61929-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61929-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61929-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61929-136">INPUTS</span></span>

### <span data-ttu-id="61929-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="61929-137">None</span></span>

## <span data-ttu-id="61929-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="61929-138">OUTPUTS</span></span>

### <span data-ttu-id="61929-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="61929-139">System.Object</span></span>
## <span data-ttu-id="61929-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="61929-140">NOTES</span></span>

## <span data-ttu-id="61929-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61929-141">RELATED LINKS</span></span>

[<span data-ttu-id="61929-142">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="61929-142">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="61929-143">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="61929-143">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="61929-144">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="61929-144">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)