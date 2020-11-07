---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: ad3ff3dbd5589a890ecf7649c9a9b66843b8b444
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786357"
---
# <span data-ttu-id="9433b-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9433b-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="9433b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9433b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9433b-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9433b-103">SYNTAX</span></span>

### <span data-ttu-id="9433b-104">Eles</span><span class="sxs-lookup"><span data-stu-id="9433b-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9433b-105">S2</span><span class="sxs-lookup"><span data-stu-id="9433b-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9433b-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9433b-106">DESCRIPTION</span></span>
<span data-ttu-id="9433b-107">O cmdlet **Restart-AzureRmWebAppSlot** interrompe e, em seguida, inicia um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9433b-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="9433b-108">Se o slot do aplicativo Web estiver em um estado parado, use o cmdlet Start-AzureRmWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="9433b-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="9433b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9433b-109">EXAMPLES</span></span>

### <span data-ttu-id="9433b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9433b-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="9433b-111">Esse comando reinicia o slot Slot001 para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="9433b-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="9433b-112">OS</span><span class="sxs-lookup"><span data-stu-id="9433b-112">PARAMETERS</span></span>

### <span data-ttu-id="9433b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9433b-113">-DefaultProfile</span></span>
<span data-ttu-id="9433b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9433b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9433b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="9433b-115">-Name</span></span>
<span data-ttu-id="9433b-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="9433b-116">WebApp Name</span></span>

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

### <span data-ttu-id="9433b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9433b-117">-ResourceGroupName</span></span>
<span data-ttu-id="9433b-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9433b-118">Resource Group Name</span></span>

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

### <span data-ttu-id="9433b-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="9433b-119">-Slot</span></span>
<span data-ttu-id="9433b-120">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="9433b-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="9433b-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9433b-121">-WebApp</span></span>
<span data-ttu-id="9433b-122">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="9433b-122">WebApp Object</span></span>

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

### <span data-ttu-id="9433b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9433b-123">CommonParameters</span></span>
<span data-ttu-id="9433b-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9433b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9433b-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9433b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9433b-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9433b-126">INPUTS</span></span>

### <span data-ttu-id="9433b-127">Instalação</span><span class="sxs-lookup"><span data-stu-id="9433b-127">Site</span></span>
<span data-ttu-id="9433b-128">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="9433b-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="9433b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9433b-129">OUTPUTS</span></span>

## <span data-ttu-id="9433b-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9433b-130">NOTES</span></span>

## <span data-ttu-id="9433b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9433b-131">RELATED LINKS</span></span>

[<span data-ttu-id="9433b-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9433b-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="9433b-133">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9433b-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="9433b-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9433b-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="9433b-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9433b-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="9433b-136">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9433b-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="9433b-137">Parar-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9433b-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="9433b-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9433b-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
