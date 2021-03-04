---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 1ce172ea2f1851f2f75a95a3037798ca3b3a2bf4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886519"
---
# <span data-ttu-id="5e969-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5e969-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="5e969-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e969-102">SYNOPSIS</span></span>
<span data-ttu-id="5e969-103">Remove um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e969-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="5e969-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5e969-104">SYNTAX</span></span>

### <span data-ttu-id="5e969-105">S1</span><span class="sxs-lookup"><span data-stu-id="5e969-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e969-106">S2</span><span class="sxs-lookup"><span data-stu-id="5e969-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e969-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5e969-107">DESCRIPTION</span></span>
<span data-ttu-id="5e969-108">O cmdlet **Remove-AzWebApp** remove um Aplicativo Web do Azure fornecido pelo grupo de recursos e pelo nome do Aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="5e969-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="5e969-109">Esse cmdlet, por padrão, também remove todos os slots e métricas.</span><span class="sxs-lookup"><span data-stu-id="5e969-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="5e969-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e969-110">EXAMPLES</span></span>

### <span data-ttu-id="5e969-111">Exemplo 1: Remover um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="5e969-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="5e969-112">Este comando remove o Aplicativo Web do Azure chamado ContosoSite que pertence ao grupo de recursos chamado Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="5e969-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="5e969-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5e969-113">PARAMETERS</span></span>

### <span data-ttu-id="5e969-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e969-114">-AsJob</span></span>
<span data-ttu-id="5e969-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5e969-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e969-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e969-116">-DefaultProfile</span></span>
<span data-ttu-id="5e969-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5e969-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e969-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5e969-118">-Force</span></span>
<span data-ttu-id="5e969-119">Opção Remover com força</span><span class="sxs-lookup"><span data-stu-id="5e969-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="5e969-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5e969-120">-Name</span></span>
<span data-ttu-id="5e969-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="5e969-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e969-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e969-122">-ResourceGroupName</span></span>
<span data-ttu-id="5e969-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="5e969-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e969-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5e969-124">-WebApp</span></span>
<span data-ttu-id="5e969-125">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="5e969-125">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e969-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e969-126">-Confirm</span></span>
<span data-ttu-id="5e969-127">Solicita a confirmação antes de executar o cmdlet. Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e969-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e969-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e969-128">-WhatIf</span></span>
<span data-ttu-id="5e969-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e969-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e969-130">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e969-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e969-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e969-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e969-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e969-132">CommonParameters</span></span>
<span data-ttu-id="5e969-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e969-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e969-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e969-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e969-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e969-135">INPUTS</span></span>

### <span data-ttu-id="5e969-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5e969-136">System.String</span></span>

### <span data-ttu-id="5e969-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="5e969-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5e969-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5e969-138">OUTPUTS</span></span>

### <span data-ttu-id="5e969-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="5e969-139">System.Void</span></span>

## <span data-ttu-id="5e969-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="5e969-140">NOTES</span></span>

## <span data-ttu-id="5e969-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e969-141">RELATED LINKS</span></span>

[<span data-ttu-id="5e969-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5e969-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="5e969-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5e969-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="5e969-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5e969-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="5e969-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5e969-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="5e969-146">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5e969-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


