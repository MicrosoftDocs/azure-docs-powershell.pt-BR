---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: eba40b4c372fd900ac42bead0e2c0b39305c91cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427757"
---
# <span data-ttu-id="ae47c-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ae47c-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="ae47c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae47c-102">SYNOPSIS</span></span>
<span data-ttu-id="ae47c-103">Interrompe um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ae47c-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="ae47c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae47c-104">SYNTAX</span></span>

### <span data-ttu-id="ae47c-105">Eles</span><span class="sxs-lookup"><span data-stu-id="ae47c-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae47c-106">S2</span><span class="sxs-lookup"><span data-stu-id="ae47c-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae47c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae47c-107">DESCRIPTION</span></span>
<span data-ttu-id="ae47c-108">O cmdlet **Stop-AzWebAppSlot** interrompe um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ae47c-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="ae47c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae47c-109">EXAMPLES</span></span>

### <span data-ttu-id="ae47c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae47c-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="ae47c-111">Esse comando interrompe o slot Slot001 pertencente ao aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="ae47c-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ae47c-112">OS</span><span class="sxs-lookup"><span data-stu-id="ae47c-112">PARAMETERS</span></span>

### <span data-ttu-id="ae47c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae47c-113">-DefaultProfile</span></span>
<span data-ttu-id="ae47c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae47c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae47c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae47c-115">-Name</span></span>
<span data-ttu-id="ae47c-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="ae47c-116">WebApp Name</span></span>

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

### <span data-ttu-id="ae47c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae47c-117">-ResourceGroupName</span></span>
<span data-ttu-id="ae47c-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ae47c-118">Resource Group Name</span></span>

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

### <span data-ttu-id="ae47c-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="ae47c-119">-Slot</span></span>
<span data-ttu-id="ae47c-120">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="ae47c-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae47c-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ae47c-121">-WebApp</span></span>
<span data-ttu-id="ae47c-122">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="ae47c-122">WebApp Object</span></span>

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

### <span data-ttu-id="ae47c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae47c-123">CommonParameters</span></span>
<span data-ttu-id="ae47c-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae47c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae47c-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae47c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae47c-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae47c-126">INPUTS</span></span>

### <span data-ttu-id="ae47c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ae47c-127">System.String</span></span>

### <span data-ttu-id="ae47c-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ae47c-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ae47c-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae47c-129">OUTPUTS</span></span>

### <span data-ttu-id="ae47c-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ae47c-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ae47c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae47c-131">NOTES</span></span>

## <span data-ttu-id="ae47c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae47c-132">RELATED LINKS</span></span>
