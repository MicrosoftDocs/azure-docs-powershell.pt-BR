---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
ms.openlocfilehash: e9b0fa9f492c64f86668688d12171795735a46dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426531"
---
# <span data-ttu-id="e8720-101">Start-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e8720-101">Start-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="e8720-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8720-102">SYNOPSIS</span></span>
<span data-ttu-id="e8720-103">Inicia um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e8720-103">Starts an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8720-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8720-104">SYNTAX</span></span>

### <span data-ttu-id="e8720-105">Eles</span><span class="sxs-lookup"><span data-stu-id="e8720-105">S1</span></span>
```
Start-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8720-106">S2</span><span class="sxs-lookup"><span data-stu-id="e8720-106">S2</span></span>
```
Start-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8720-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8720-107">DESCRIPTION</span></span>
<span data-ttu-id="e8720-108">O cmdlet **Start-AzureRmWebAppSlot** inicia um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e8720-108">The **Start-AzureRmWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="e8720-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8720-109">EXAMPLES</span></span>

### <span data-ttu-id="e8720-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e8720-110">Example 1</span></span>
```
PS C:\>Start-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="e8720-111">Esse comando inicia o slot chamado Slot001 relativo ao aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="e8720-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e8720-112">OS</span><span class="sxs-lookup"><span data-stu-id="e8720-112">PARAMETERS</span></span>

### <span data-ttu-id="e8720-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8720-113">-DefaultProfile</span></span>
<span data-ttu-id="e8720-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8720-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8720-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8720-115">-Name</span></span>
<span data-ttu-id="e8720-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="e8720-116">WebApp Name</span></span>

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

### <span data-ttu-id="e8720-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8720-117">-ResourceGroupName</span></span>
<span data-ttu-id="e8720-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e8720-118">Resource Group Name</span></span>

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

### <span data-ttu-id="e8720-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="e8720-119">-Slot</span></span>
<span data-ttu-id="e8720-120">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="e8720-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8720-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e8720-121">-WebApp</span></span>
<span data-ttu-id="e8720-122">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="e8720-122">WebApp Object</span></span>

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

### <span data-ttu-id="e8720-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8720-123">CommonParameters</span></span>
<span data-ttu-id="e8720-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8720-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8720-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8720-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8720-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8720-126">INPUTS</span></span>

### <span data-ttu-id="e8720-127">Instalação</span><span class="sxs-lookup"><span data-stu-id="e8720-127">Site</span></span>
<span data-ttu-id="e8720-128">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="e8720-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e8720-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8720-129">OUTPUTS</span></span>

## <span data-ttu-id="e8720-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8720-130">NOTES</span></span>

## <span data-ttu-id="e8720-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8720-131">RELATED LINKS</span></span>

[<span data-ttu-id="e8720-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e8720-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="e8720-133">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e8720-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="e8720-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e8720-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="e8720-135">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e8720-135">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="e8720-136">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e8720-136">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="e8720-137">Parar-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e8720-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="e8720-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e8720-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
