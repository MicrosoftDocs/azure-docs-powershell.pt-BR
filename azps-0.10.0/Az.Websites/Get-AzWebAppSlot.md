---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 033b0bd4458f20153ec1e9c876f12c7e7c368c0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776103"
---
# <span data-ttu-id="6eced-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6eced-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="6eced-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6eced-102">SYNOPSIS</span></span>
<span data-ttu-id="6eced-103">Obtém um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="6eced-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="6eced-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6eced-104">SYNTAX</span></span>

### <span data-ttu-id="6eced-105">Eles</span><span class="sxs-lookup"><span data-stu-id="6eced-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6eced-106">S2</span><span class="sxs-lookup"><span data-stu-id="6eced-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6eced-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6eced-107">DESCRIPTION</span></span>
<span data-ttu-id="6eced-108">O cmdlet **Get-AzWebAppSlot** Obtém informações sobre um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="6eced-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="6eced-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6eced-109">EXAMPLES</span></span>

### <span data-ttu-id="6eced-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6eced-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="6eced-111">Esse comando obtém o slot chamado Slot001 do aplicativo Web nomeado WebAppStandard que pertence ao grupo de recursos padrão-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="6eced-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="6eced-112">OS</span><span class="sxs-lookup"><span data-stu-id="6eced-112">PARAMETERS</span></span>

### <span data-ttu-id="6eced-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eced-113">-DefaultProfile</span></span>
<span data-ttu-id="6eced-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6eced-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eced-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6eced-115">-Name</span></span>
<span data-ttu-id="6eced-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="6eced-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eced-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eced-117">-ResourceGroupName</span></span>
<span data-ttu-id="6eced-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6eced-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eced-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="6eced-119">-Slot</span></span>
<span data-ttu-id="6eced-120">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="6eced-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eced-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6eced-121">-WebApp</span></span>
<span data-ttu-id="6eced-122">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="6eced-122">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6eced-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eced-123">CommonParameters</span></span>
<span data-ttu-id="6eced-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eced-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eced-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eced-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eced-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6eced-126">INPUTS</span></span>

### <span data-ttu-id="6eced-127">Instalação</span><span class="sxs-lookup"><span data-stu-id="6eced-127">Site</span></span>
<span data-ttu-id="6eced-128">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="6eced-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6eced-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6eced-129">OUTPUTS</span></span>

## <span data-ttu-id="6eced-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6eced-130">NOTES</span></span>

## <span data-ttu-id="6eced-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6eced-131">RELATED LINKS</span></span>

[<span data-ttu-id="6eced-132">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6eced-132">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="6eced-133">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6eced-133">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="6eced-134">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6eced-134">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="6eced-135">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6eced-135">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="6eced-136">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6eced-136">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="6eced-137">Parar-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6eced-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="6eced-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6eced-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
