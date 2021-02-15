---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: faa3264dbf9fa65a2970f578c635868d185f2ef8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118834"
---
# <span data-ttu-id="d88e9-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d88e9-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="d88e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d88e9-102">SYNOPSIS</span></span>
<span data-ttu-id="d88e9-103">Reinicia um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d88e9-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="d88e9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d88e9-104">SYNTAX</span></span>

### <span data-ttu-id="d88e9-105">S1</span><span class="sxs-lookup"><span data-stu-id="d88e9-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d88e9-106">S2</span><span class="sxs-lookup"><span data-stu-id="d88e9-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d88e9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d88e9-107">DESCRIPTION</span></span>
<span data-ttu-id="d88e9-108">O cmdlet **Restart-AzWebApp** para e inicia um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d88e9-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="d88e9-109">Se o Web App estiver em um estado interrompido, use o cmdlet Start-AzWebApp web app.</span><span class="sxs-lookup"><span data-stu-id="d88e9-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="d88e9-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d88e9-110">EXAMPLES</span></span>

### <span data-ttu-id="d88e9-111">Exemplo 1: Reiniciar um Aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="d88e9-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="d88e9-112">Esse comando interrompe o Azure Web App chamado ContosoSite que pertence ao grupo de recursos chamado Default-Web-WestUS e o reinicia.</span><span class="sxs-lookup"><span data-stu-id="d88e9-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="d88e9-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d88e9-113">PARAMETERS</span></span>

### <span data-ttu-id="d88e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d88e9-114">-DefaultProfile</span></span>
<span data-ttu-id="d88e9-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d88e9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d88e9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d88e9-116">-Name</span></span>
<span data-ttu-id="d88e9-117">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="d88e9-117">WebApp Name</span></span>

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

### <span data-ttu-id="d88e9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d88e9-118">-ResourceGroupName</span></span>
<span data-ttu-id="d88e9-119">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d88e9-119">Resource Group Name</span></span>

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

### <span data-ttu-id="d88e9-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d88e9-120">-WebApp</span></span>
<span data-ttu-id="d88e9-121">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="d88e9-121">WebApp Object</span></span>

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

### <span data-ttu-id="d88e9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d88e9-122">CommonParameters</span></span>
<span data-ttu-id="d88e9-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d88e9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d88e9-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d88e9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d88e9-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="d88e9-125">INPUTS</span></span>

### <span data-ttu-id="d88e9-126">System.String</span><span class="sxs-lookup"><span data-stu-id="d88e9-126">System.String</span></span>

### <span data-ttu-id="d88e9-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="d88e9-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d88e9-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="d88e9-128">OUTPUTS</span></span>

### <span data-ttu-id="d88e9-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="d88e9-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d88e9-130">Notas</span><span class="sxs-lookup"><span data-stu-id="d88e9-130">NOTES</span></span>

## <span data-ttu-id="d88e9-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d88e9-131">RELATED LINKS</span></span>

[<span data-ttu-id="d88e9-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d88e9-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="d88e9-133">Novo-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d88e9-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="d88e9-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d88e9-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="d88e9-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d88e9-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="d88e9-136">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d88e9-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


