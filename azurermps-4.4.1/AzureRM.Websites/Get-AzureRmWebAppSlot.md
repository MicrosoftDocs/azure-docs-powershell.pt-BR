---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
ms.openlocfilehash: 841cc1f8356d9b082dec55e689033c19343041d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429011"
---
# <span data-ttu-id="93d84-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="93d84-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="93d84-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93d84-102">SYNOPSIS</span></span>
<span data-ttu-id="93d84-103">Obtém um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="93d84-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93d84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93d84-104">SYNTAX</span></span>

### <span data-ttu-id="93d84-105">Eles</span><span class="sxs-lookup"><span data-stu-id="93d84-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93d84-106">S2</span><span class="sxs-lookup"><span data-stu-id="93d84-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93d84-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93d84-107">DESCRIPTION</span></span>
<span data-ttu-id="93d84-108">O cmdlet **Get-AzureRmWebAppSlot** Obtém informações sobre um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="93d84-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="93d84-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93d84-109">EXAMPLES</span></span>

### <span data-ttu-id="93d84-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="93d84-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="93d84-111">Esse comando obtém o slot chamado Slot001 do aplicativo Web nomeado WebAppStandard que pertence ao grupo de recursos padrão-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="93d84-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="93d84-112">OS</span><span class="sxs-lookup"><span data-stu-id="93d84-112">PARAMETERS</span></span>

### <span data-ttu-id="93d84-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="93d84-113">-Name</span></span>
<span data-ttu-id="93d84-114">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="93d84-114">WebApp Name</span></span>

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

### <span data-ttu-id="93d84-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93d84-115">-ResourceGroupName</span></span>
<span data-ttu-id="93d84-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="93d84-116">Resource Group Name</span></span>

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

### <span data-ttu-id="93d84-117">-Slot</span><span class="sxs-lookup"><span data-stu-id="93d84-117">-Slot</span></span>
<span data-ttu-id="93d84-118">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="93d84-118">WebApp Slot Name</span></span>

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

### <span data-ttu-id="93d84-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="93d84-119">-WebApp</span></span>
<span data-ttu-id="93d84-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="93d84-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93d84-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93d84-121">-DefaultProfile</span></span>
<span data-ttu-id="93d84-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93d84-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93d84-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d84-123">CommonParameters</span></span>
<span data-ttu-id="93d84-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93d84-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d84-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93d84-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d84-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93d84-126">INPUTS</span></span>

### <span data-ttu-id="93d84-127">Instalação</span><span class="sxs-lookup"><span data-stu-id="93d84-127">Site</span></span>
<span data-ttu-id="93d84-128">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="93d84-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="93d84-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93d84-129">OUTPUTS</span></span>

## <span data-ttu-id="93d84-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93d84-130">NOTES</span></span>

## <span data-ttu-id="93d84-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93d84-131">RELATED LINKS</span></span>

[<span data-ttu-id="93d84-132">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="93d84-132">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="93d84-133">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="93d84-133">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="93d84-134">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="93d84-134">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="93d84-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="93d84-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="93d84-136">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="93d84-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="93d84-137">Parar-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="93d84-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="93d84-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="93d84-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
