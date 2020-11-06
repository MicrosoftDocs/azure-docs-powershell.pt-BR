---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
ms.openlocfilehash: f7be5b7877362484d0f3dfe4d19b8afc669e917c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426248"
---
# <span data-ttu-id="208f2-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="208f2-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="208f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="208f2-102">SYNOPSIS</span></span>
<span data-ttu-id="208f2-103">Obtém um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="208f2-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="208f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="208f2-104">SYNTAX</span></span>

### <span data-ttu-id="208f2-105">Eles</span><span class="sxs-lookup"><span data-stu-id="208f2-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="208f2-106">S2</span><span class="sxs-lookup"><span data-stu-id="208f2-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="208f2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="208f2-107">DESCRIPTION</span></span>
<span data-ttu-id="208f2-108">O cmdlet **Get-AzureRmWebAppSlot** Obtém informações sobre um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="208f2-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="208f2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="208f2-109">EXAMPLES</span></span>

### <span data-ttu-id="208f2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="208f2-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="208f2-111">Esse comando obtém o slot chamado Slot001 do aplicativo Web nomeado WebAppStandard que pertence ao grupo de recursos padrão-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="208f2-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="208f2-112">OS</span><span class="sxs-lookup"><span data-stu-id="208f2-112">PARAMETERS</span></span>

### <span data-ttu-id="208f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="208f2-113">-DefaultProfile</span></span>
<span data-ttu-id="208f2-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="208f2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208f2-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="208f2-115">-Name</span></span>
<span data-ttu-id="208f2-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="208f2-116">WebApp Name</span></span>

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

### <span data-ttu-id="208f2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="208f2-117">-ResourceGroupName</span></span>
<span data-ttu-id="208f2-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="208f2-118">Resource Group Name</span></span>

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

### <span data-ttu-id="208f2-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="208f2-119">-Slot</span></span>
<span data-ttu-id="208f2-120">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="208f2-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208f2-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="208f2-121">-WebApp</span></span>
<span data-ttu-id="208f2-122">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="208f2-122">WebApp Object</span></span>

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

### <span data-ttu-id="208f2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="208f2-123">CommonParameters</span></span>
<span data-ttu-id="208f2-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="208f2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="208f2-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="208f2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="208f2-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="208f2-126">INPUTS</span></span>

### <span data-ttu-id="208f2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="208f2-127">System.String</span></span>

### <span data-ttu-id="208f2-128">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="208f2-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="208f2-129">Parâmetros: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="208f2-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="208f2-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="208f2-130">OUTPUTS</span></span>

### <span data-ttu-id="208f2-131">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="208f2-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="208f2-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="208f2-132">NOTES</span></span>

## <span data-ttu-id="208f2-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="208f2-133">RELATED LINKS</span></span>

[<span data-ttu-id="208f2-134">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="208f2-134">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="208f2-135">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="208f2-135">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="208f2-136">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="208f2-136">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="208f2-137">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="208f2-137">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="208f2-138">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="208f2-138">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="208f2-139">Parar-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="208f2-139">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="208f2-140">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="208f2-140">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
