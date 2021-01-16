---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 840e0bb2bfa10a89a5ba963e83ab434e795b3dd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257137"
---
# <span data-ttu-id="ef629-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="ef629-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="ef629-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef629-102">SYNOPSIS</span></span>

## <span data-ttu-id="ef629-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef629-103">SYNTAX</span></span>

### <span data-ttu-id="ef629-104">Eles</span><span class="sxs-lookup"><span data-stu-id="ef629-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef629-105">S2</span><span class="sxs-lookup"><span data-stu-id="ef629-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef629-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef629-106">DESCRIPTION</span></span>
<span data-ttu-id="ef629-107">O cmdlet **Reset-AzWebAppSlotPublishingProfile** redefine o perfil de publicação para o slot do aplicativo Web especificado.</span><span class="sxs-lookup"><span data-stu-id="ef629-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="ef629-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef629-108">EXAMPLES</span></span>

### <span data-ttu-id="ef629-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ef629-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="ef629-110">Esse comando redefine o perfil de publicação do slot chamado slot001 para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="ef629-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="ef629-111">OS</span><span class="sxs-lookup"><span data-stu-id="ef629-111">PARAMETERS</span></span>

### <span data-ttu-id="ef629-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef629-112">-DefaultProfile</span></span>
<span data-ttu-id="ef629-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef629-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef629-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef629-114">-Name</span></span>
<span data-ttu-id="ef629-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="ef629-115">WebApp Name</span></span>

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

### <span data-ttu-id="ef629-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef629-116">-ResourceGroupName</span></span>
<span data-ttu-id="ef629-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ef629-117">Resource Group Name</span></span>

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

### <span data-ttu-id="ef629-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="ef629-118">-Slot</span></span>
<span data-ttu-id="ef629-119">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="ef629-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ef629-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ef629-120">-WebApp</span></span>
<span data-ttu-id="ef629-121">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="ef629-121">WebApp Object</span></span>

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

### <span data-ttu-id="ef629-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef629-122">CommonParameters</span></span>
<span data-ttu-id="ef629-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef629-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef629-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef629-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef629-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef629-125">INPUTS</span></span>

### <span data-ttu-id="ef629-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ef629-126">System.String</span></span>

### <span data-ttu-id="ef629-127">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ef629-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ef629-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef629-128">OUTPUTS</span></span>

### <span data-ttu-id="ef629-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ef629-129">System.String</span></span>

## <span data-ttu-id="ef629-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef629-130">NOTES</span></span>

## <span data-ttu-id="ef629-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef629-131">RELATED LINKS</span></span>
