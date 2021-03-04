---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServiceEnvironment.md
ms.openlocfilehash: 9641c55dd25d8f09d1898bdda37fafa840db0a19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889373"
---
# <span data-ttu-id="a8d44-101">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="a8d44-101">Get-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="a8d44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8d44-102">SYNOPSIS</span></span>
<span data-ttu-id="a8d44-103">Obtém o ambiente de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a8d44-103">Gets App Service Environment.</span></span> <span data-ttu-id="a8d44-104">Se apenas o Grupo de Recursos for especificado, ele retornará uma lista de ASE no Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="a8d44-104">If only Resource Group is specified, it will return a list of ASE in the Resource Group.</span></span>

## <span data-ttu-id="a8d44-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a8d44-105">SYNTAX</span></span>

```
Get-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8d44-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a8d44-106">DESCRIPTION</span></span>
<span data-ttu-id="a8d44-107">O cmdlet **Get-AzAppServiceEnvironment** retorna ASE(s) correspondente à consulta.</span><span class="sxs-lookup"><span data-stu-id="a8d44-107">The **Get-AzAppServiceEnvironment** cmdlet return ASE(s) matching the query.</span></span>

## <span data-ttu-id="a8d44-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8d44-108">EXAMPLES</span></span>

### <span data-ttu-id="a8d44-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a8d44-109">Example 1</span></span>
```powershell
PS C:\> Get-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseName
```

<span data-ttu-id="a8d44-110">Retorna um ambiente de serviço de aplicativo específico <MyAseName> chamado em <MyResourceGroup></span><span class="sxs-lookup"><span data-stu-id="a8d44-110">Returns a specific App Service Environment named <MyAseName> in <MyResourceGroup></span></span>

## <span data-ttu-id="a8d44-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a8d44-111">PARAMETERS</span></span>

### <span data-ttu-id="a8d44-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8d44-112">-DefaultProfile</span></span>
<span data-ttu-id="a8d44-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a8d44-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8d44-114">-Name</span><span class="sxs-lookup"><span data-stu-id="a8d44-114">-Name</span></span>
<span data-ttu-id="a8d44-115">O nome do ambiente de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a8d44-115">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8d44-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8d44-116">-ResourceGroupName</span></span>
<span data-ttu-id="a8d44-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a8d44-117">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8d44-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8d44-118">-Confirm</span></span>
<span data-ttu-id="a8d44-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8d44-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8d44-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8d44-120">-WhatIf</span></span>
<span data-ttu-id="a8d44-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a8d44-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8d44-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a8d44-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8d44-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8d44-123">CommonParameters</span></span>
<span data-ttu-id="a8d44-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8d44-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8d44-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8d44-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8d44-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8d44-126">INPUTS</span></span>

### <span data-ttu-id="a8d44-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a8d44-127">None</span></span>

## <span data-ttu-id="a8d44-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a8d44-128">OUTPUTS</span></span>

### <span data-ttu-id="a8d44-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="a8d44-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment</span></span>

## <span data-ttu-id="a8d44-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="a8d44-130">NOTES</span></span>

## <span data-ttu-id="a8d44-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8d44-131">RELATED LINKS</span></span>

[<span data-ttu-id="a8d44-132">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="a8d44-132">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="a8d44-133">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="a8d44-133">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)

[<span data-ttu-id="a8d44-134">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="a8d44-134">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)