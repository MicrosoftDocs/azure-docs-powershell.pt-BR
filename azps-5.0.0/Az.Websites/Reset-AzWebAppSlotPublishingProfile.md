---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 840e0bb2bfa10a89a5ba963e83ab434e795b3dd4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125188"
---
# <span data-ttu-id="a18d3-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="a18d3-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="a18d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a18d3-102">SYNOPSIS</span></span>

## <span data-ttu-id="a18d3-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a18d3-103">SYNTAX</span></span>

### <span data-ttu-id="a18d3-104">Eles</span><span class="sxs-lookup"><span data-stu-id="a18d3-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a18d3-105">S2</span><span class="sxs-lookup"><span data-stu-id="a18d3-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a18d3-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a18d3-106">DESCRIPTION</span></span>
<span data-ttu-id="a18d3-107">O cmdlet **Reset-AzWebAppSlotPublishingProfile** redefine o perfil de publicação para o slot do aplicativo Web especificado.</span><span class="sxs-lookup"><span data-stu-id="a18d3-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="a18d3-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a18d3-108">EXAMPLES</span></span>

### <span data-ttu-id="a18d3-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a18d3-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="a18d3-110">Esse comando redefine o perfil de publicação do slot chamado slot001 para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="a18d3-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a18d3-111">OS</span><span class="sxs-lookup"><span data-stu-id="a18d3-111">PARAMETERS</span></span>

### <span data-ttu-id="a18d3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a18d3-112">-DefaultProfile</span></span>
<span data-ttu-id="a18d3-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a18d3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a18d3-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="a18d3-114">-Name</span></span>
<span data-ttu-id="a18d3-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="a18d3-115">WebApp Name</span></span>

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

### <span data-ttu-id="a18d3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a18d3-116">-ResourceGroupName</span></span>
<span data-ttu-id="a18d3-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a18d3-117">Resource Group Name</span></span>

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

### <span data-ttu-id="a18d3-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="a18d3-118">-Slot</span></span>
<span data-ttu-id="a18d3-119">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="a18d3-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="a18d3-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a18d3-120">-WebApp</span></span>
<span data-ttu-id="a18d3-121">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="a18d3-121">WebApp Object</span></span>

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

### <span data-ttu-id="a18d3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a18d3-122">CommonParameters</span></span>
<span data-ttu-id="a18d3-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a18d3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a18d3-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a18d3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a18d3-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a18d3-125">INPUTS</span></span>

### <span data-ttu-id="a18d3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a18d3-126">System.String</span></span>

### <span data-ttu-id="a18d3-127">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="a18d3-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a18d3-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a18d3-128">OUTPUTS</span></span>

### <span data-ttu-id="a18d3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a18d3-129">System.String</span></span>

## <span data-ttu-id="a18d3-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a18d3-130">NOTES</span></span>

## <span data-ttu-id="a18d3-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a18d3-131">RELATED LINKS</span></span>
