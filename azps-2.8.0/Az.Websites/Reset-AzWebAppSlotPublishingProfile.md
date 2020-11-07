---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 0d67d2de8aebd251f4c02f19ff6a544325f2db5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774077"
---
# <span data-ttu-id="dbc0c-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="dbc0c-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="dbc0c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dbc0c-102">SYNOPSIS</span></span>

## <span data-ttu-id="dbc0c-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbc0c-103">SYNTAX</span></span>

### <span data-ttu-id="dbc0c-104">Eles</span><span class="sxs-lookup"><span data-stu-id="dbc0c-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbc0c-105">S2</span><span class="sxs-lookup"><span data-stu-id="dbc0c-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dbc0c-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dbc0c-106">DESCRIPTION</span></span>
<span data-ttu-id="dbc0c-107">O cmdlet **Reset-AzWebAppSlotPublishingProfile** redefine o perfil de publicação para o slot do aplicativo Web especificado.</span><span class="sxs-lookup"><span data-stu-id="dbc0c-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="dbc0c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dbc0c-108">EXAMPLES</span></span>

### <span data-ttu-id="dbc0c-109">1:</span><span class="sxs-lookup"><span data-stu-id="dbc0c-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="dbc0c-110">Esse comando redefine o perfil de publicação do slot chamado slot001 para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="dbc0c-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="dbc0c-111">OS</span><span class="sxs-lookup"><span data-stu-id="dbc0c-111">PARAMETERS</span></span>

### <span data-ttu-id="dbc0c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc0c-112">-DefaultProfile</span></span>
<span data-ttu-id="dbc0c-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dbc0c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbc0c-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="dbc0c-114">-Name</span></span>
<span data-ttu-id="dbc0c-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="dbc0c-115">WebApp Name</span></span>

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

### <span data-ttu-id="dbc0c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbc0c-116">-ResourceGroupName</span></span>
<span data-ttu-id="dbc0c-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="dbc0c-117">Resource Group Name</span></span>

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

### <span data-ttu-id="dbc0c-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="dbc0c-118">-Slot</span></span>
<span data-ttu-id="dbc0c-119">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="dbc0c-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="dbc0c-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="dbc0c-120">-WebApp</span></span>
<span data-ttu-id="dbc0c-121">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="dbc0c-121">WebApp Object</span></span>

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

### <span data-ttu-id="dbc0c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc0c-122">CommonParameters</span></span>
<span data-ttu-id="dbc0c-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbc0c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc0c-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbc0c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc0c-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dbc0c-125">INPUTS</span></span>

### <span data-ttu-id="dbc0c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="dbc0c-126">System.String</span></span>

### <span data-ttu-id="dbc0c-127">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="dbc0c-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="dbc0c-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dbc0c-128">OUTPUTS</span></span>

### <span data-ttu-id="dbc0c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="dbc0c-129">System.String</span></span>

## <span data-ttu-id="dbc0c-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dbc0c-130">NOTES</span></span>

## <span data-ttu-id="dbc0c-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dbc0c-131">RELATED LINKS</span></span>
