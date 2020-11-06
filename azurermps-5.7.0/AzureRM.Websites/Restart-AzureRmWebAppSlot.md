---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
ms.openlocfilehash: 08e5f0e1ba87f42f8a2893a63f8f853ece9870c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609467"
---
# <span data-ttu-id="45b43-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45b43-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="45b43-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45b43-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45b43-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45b43-103">SYNTAX</span></span>

### <span data-ttu-id="45b43-104">Eles</span><span class="sxs-lookup"><span data-stu-id="45b43-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45b43-105">S2</span><span class="sxs-lookup"><span data-stu-id="45b43-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45b43-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45b43-106">DESCRIPTION</span></span>
<span data-ttu-id="45b43-107">O cmdlet **Restart-AzureRmWebAppSlot** interrompe e, em seguida, inicia um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="45b43-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="45b43-108">Se o slot do aplicativo Web estiver em um estado parado, use o cmdlet Start-AzureRmWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="45b43-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="45b43-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45b43-109">EXAMPLES</span></span>

### <span data-ttu-id="45b43-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="45b43-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="45b43-111">Esse comando reinicia o slot Slot001 para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="45b43-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="45b43-112">OS</span><span class="sxs-lookup"><span data-stu-id="45b43-112">PARAMETERS</span></span>

### <span data-ttu-id="45b43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b43-113">-DefaultProfile</span></span>
<span data-ttu-id="45b43-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45b43-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45b43-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="45b43-115">-Name</span></span>
<span data-ttu-id="45b43-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="45b43-116">WebApp Name</span></span>

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

### <span data-ttu-id="45b43-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45b43-117">-ResourceGroupName</span></span>
<span data-ttu-id="45b43-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="45b43-118">Resource Group Name</span></span>

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

### <span data-ttu-id="45b43-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="45b43-119">-Slot</span></span>
<span data-ttu-id="45b43-120">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="45b43-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="45b43-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="45b43-121">-WebApp</span></span>
<span data-ttu-id="45b43-122">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="45b43-122">WebApp Object</span></span>

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

### <span data-ttu-id="45b43-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b43-123">CommonParameters</span></span>
<span data-ttu-id="45b43-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b43-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b43-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45b43-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b43-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45b43-126">INPUTS</span></span>

### <span data-ttu-id="45b43-127">Instalação</span><span class="sxs-lookup"><span data-stu-id="45b43-127">Site</span></span>
<span data-ttu-id="45b43-128">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="45b43-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="45b43-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45b43-129">OUTPUTS</span></span>

## <span data-ttu-id="45b43-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45b43-130">NOTES</span></span>

## <span data-ttu-id="45b43-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45b43-131">RELATED LINKS</span></span>

[<span data-ttu-id="45b43-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45b43-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="45b43-133">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45b43-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="45b43-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45b43-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="45b43-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45b43-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="45b43-136">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45b43-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="45b43-137">Parar-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45b43-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="45b43-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="45b43-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
