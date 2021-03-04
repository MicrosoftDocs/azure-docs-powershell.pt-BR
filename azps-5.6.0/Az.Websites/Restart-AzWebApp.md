---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: e155a58420d9f190bfebdb21272d64dab1f3c21f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891914"
---
# <span data-ttu-id="7e5eb-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7e5eb-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="7e5eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e5eb-102">SYNOPSIS</span></span>
<span data-ttu-id="7e5eb-103">Reinicia um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="7e5eb-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="7e5eb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7e5eb-104">SYNTAX</span></span>

### <span data-ttu-id="7e5eb-105">S1</span><span class="sxs-lookup"><span data-stu-id="7e5eb-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e5eb-106">S2</span><span class="sxs-lookup"><span data-stu-id="7e5eb-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e5eb-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7e5eb-107">DESCRIPTION</span></span>
<span data-ttu-id="7e5eb-108">O cmdlet **Restart-AzWebApp** para e inicia um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="7e5eb-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="7e5eb-109">Se o Aplicativo Web estiver em um estado parado, use o cmdlet Start-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="7e5eb-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="7e5eb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e5eb-110">EXAMPLES</span></span>

### <span data-ttu-id="7e5eb-111">Exemplo 1: reiniciar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="7e5eb-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="7e5eb-112">Este comando interrompe o Aplicativo Web do Azure chamado ContosoSite que pertence ao grupo de recursos chamado Default-Web-WestUS e o reinicia.</span><span class="sxs-lookup"><span data-stu-id="7e5eb-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="7e5eb-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7e5eb-113">PARAMETERS</span></span>

### <span data-ttu-id="7e5eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e5eb-114">-DefaultProfile</span></span>
<span data-ttu-id="7e5eb-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7e5eb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e5eb-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7e5eb-116">-Name</span></span>
<span data-ttu-id="7e5eb-117">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="7e5eb-117">WebApp Name</span></span>

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

### <span data-ttu-id="7e5eb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e5eb-118">-ResourceGroupName</span></span>
<span data-ttu-id="7e5eb-119">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7e5eb-119">Resource Group Name</span></span>

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

### <span data-ttu-id="7e5eb-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7e5eb-120">-WebApp</span></span>
<span data-ttu-id="7e5eb-121">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="7e5eb-121">WebApp Object</span></span>

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

### <span data-ttu-id="7e5eb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e5eb-122">CommonParameters</span></span>
<span data-ttu-id="7e5eb-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e5eb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e5eb-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e5eb-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e5eb-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e5eb-125">INPUTS</span></span>

### <span data-ttu-id="7e5eb-126">System.String</span><span class="sxs-lookup"><span data-stu-id="7e5eb-126">System.String</span></span>

### <span data-ttu-id="7e5eb-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="7e5eb-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7e5eb-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7e5eb-128">OUTPUTS</span></span>

### <span data-ttu-id="7e5eb-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="7e5eb-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7e5eb-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="7e5eb-130">NOTES</span></span>

## <span data-ttu-id="7e5eb-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e5eb-131">RELATED LINKS</span></span>

[<span data-ttu-id="7e5eb-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7e5eb-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="7e5eb-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7e5eb-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="7e5eb-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7e5eb-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="7e5eb-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7e5eb-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="7e5eb-136">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7e5eb-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


