---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 64d463e6cbe3012b8d49e0a61b4f081f286e25b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427798"
---
# <span data-ttu-id="e2b65-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e2b65-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="e2b65-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2b65-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b65-103">Remove um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2b65-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="e2b65-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2b65-104">SYNTAX</span></span>

### <span data-ttu-id="e2b65-105">Eles</span><span class="sxs-lookup"><span data-stu-id="e2b65-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2b65-106">S2</span><span class="sxs-lookup"><span data-stu-id="e2b65-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2b65-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2b65-107">DESCRIPTION</span></span>
<span data-ttu-id="e2b65-108">O cmdlet **Remove-AzWebApp** remove um aplicativo Web do Azure desde o grupo de recursos e o nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="e2b65-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="e2b65-109">Esse cmdlet, por padrão, também remove todos os slots e métricas.</span><span class="sxs-lookup"><span data-stu-id="e2b65-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="e2b65-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2b65-110">EXAMPLES</span></span>

### <span data-ttu-id="e2b65-111">Exemplo 1: remover um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="e2b65-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="e2b65-112">Esse comando Remove o aplicativo Web do Azure chamado ContosoSite que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="e2b65-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e2b65-113">OS</span><span class="sxs-lookup"><span data-stu-id="e2b65-113">PARAMETERS</span></span>

### <span data-ttu-id="e2b65-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2b65-114">-AsJob</span></span>
<span data-ttu-id="e2b65-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e2b65-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2b65-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b65-116">-DefaultProfile</span></span>
<span data-ttu-id="e2b65-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2b65-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2b65-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e2b65-118">-Force</span></span>
<span data-ttu-id="e2b65-119">Opção de remoção forçada</span><span class="sxs-lookup"><span data-stu-id="e2b65-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="e2b65-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2b65-120">-Name</span></span>
<span data-ttu-id="e2b65-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="e2b65-121">WebApp Name</span></span>

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

### <span data-ttu-id="e2b65-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2b65-122">-ResourceGroupName</span></span>
<span data-ttu-id="e2b65-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e2b65-123">Resource Group Name</span></span>

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

### <span data-ttu-id="e2b65-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e2b65-124">-WebApp</span></span>
<span data-ttu-id="e2b65-125">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="e2b65-125">WebApp Object</span></span>

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

### <span data-ttu-id="e2b65-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e2b65-126">-Confirm</span></span>
<span data-ttu-id="e2b65-127">Solicita confirmação antes de executar o cmdlet. Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2b65-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2b65-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2b65-128">-WhatIf</span></span>
<span data-ttu-id="e2b65-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e2b65-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2b65-130">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e2b65-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2b65-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e2b65-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2b65-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b65-132">CommonParameters</span></span>
<span data-ttu-id="e2b65-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2b65-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b65-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2b65-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b65-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2b65-135">INPUTS</span></span>

### <span data-ttu-id="e2b65-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e2b65-136">System.String</span></span>

### <span data-ttu-id="e2b65-137">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="e2b65-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e2b65-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2b65-138">OUTPUTS</span></span>

### <span data-ttu-id="e2b65-139">System. void</span><span class="sxs-lookup"><span data-stu-id="e2b65-139">System.Void</span></span>

## <span data-ttu-id="e2b65-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2b65-140">NOTES</span></span>

## <span data-ttu-id="e2b65-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2b65-141">RELATED LINKS</span></span>

[<span data-ttu-id="e2b65-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e2b65-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="e2b65-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e2b65-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="e2b65-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e2b65-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="e2b65-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e2b65-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="e2b65-146">Parar-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e2b65-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


