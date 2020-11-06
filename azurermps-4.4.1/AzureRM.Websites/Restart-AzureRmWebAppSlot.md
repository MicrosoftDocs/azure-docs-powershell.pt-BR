---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
ms.openlocfilehash: ace1b16bc6d89fb619daba23a214326acd8d0d24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426866"
---
# <span data-ttu-id="56c9e-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56c9e-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="56c9e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56c9e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56c9e-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56c9e-103">SYNTAX</span></span>

### <span data-ttu-id="56c9e-104">Eles</span><span class="sxs-lookup"><span data-stu-id="56c9e-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56c9e-105">S2</span><span class="sxs-lookup"><span data-stu-id="56c9e-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56c9e-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="56c9e-106">DESCRIPTION</span></span>
<span data-ttu-id="56c9e-107">O cmdlet **Restart-AzureRmWebAppSlot** interrompe e, em seguida, inicia um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="56c9e-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="56c9e-108">Se o slot do aplicativo Web estiver em um estado parado, use o cmdlet Start-AzureRmWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="56c9e-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="56c9e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56c9e-109">EXAMPLES</span></span>

### <span data-ttu-id="56c9e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="56c9e-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="56c9e-111">Esse comando reinicia o slot Slot001 para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="56c9e-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="56c9e-112">OS</span><span class="sxs-lookup"><span data-stu-id="56c9e-112">PARAMETERS</span></span>

### <span data-ttu-id="56c9e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="56c9e-113">-Name</span></span>
<span data-ttu-id="56c9e-114">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="56c9e-114">WebApp Name</span></span>

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

### <span data-ttu-id="56c9e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56c9e-115">-ResourceGroupName</span></span>
<span data-ttu-id="56c9e-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="56c9e-116">Resource Group Name</span></span>

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

### <span data-ttu-id="56c9e-117">-Slot</span><span class="sxs-lookup"><span data-stu-id="56c9e-117">-Slot</span></span>
<span data-ttu-id="56c9e-118">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="56c9e-118">WebApp Slot Name</span></span>

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

### <span data-ttu-id="56c9e-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="56c9e-119">-WebApp</span></span>
<span data-ttu-id="56c9e-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="56c9e-120">WebApp Object</span></span>

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

### <span data-ttu-id="56c9e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56c9e-121">-DefaultProfile</span></span>
<span data-ttu-id="56c9e-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56c9e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56c9e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c9e-123">CommonParameters</span></span>
<span data-ttu-id="56c9e-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56c9e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56c9e-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56c9e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c9e-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="56c9e-126">INPUTS</span></span>

### <span data-ttu-id="56c9e-127">Instalação</span><span class="sxs-lookup"><span data-stu-id="56c9e-127">Site</span></span>
<span data-ttu-id="56c9e-128">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="56c9e-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="56c9e-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="56c9e-129">OUTPUTS</span></span>

## <span data-ttu-id="56c9e-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="56c9e-130">NOTES</span></span>

## <span data-ttu-id="56c9e-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56c9e-131">RELATED LINKS</span></span>

[<span data-ttu-id="56c9e-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56c9e-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="56c9e-133">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56c9e-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="56c9e-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56c9e-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="56c9e-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56c9e-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="56c9e-136">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56c9e-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="56c9e-137">Parar-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56c9e-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="56c9e-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="56c9e-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
