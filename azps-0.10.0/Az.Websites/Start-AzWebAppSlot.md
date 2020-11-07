---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/start-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: d843cf5eed70e230f81c704e9168fee917a77077
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776059"
---
# <span data-ttu-id="b684d-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b684d-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="b684d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b684d-102">SYNOPSIS</span></span>
<span data-ttu-id="b684d-103">Inicia um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b684d-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="b684d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b684d-104">SYNTAX</span></span>

### <span data-ttu-id="b684d-105">Eles</span><span class="sxs-lookup"><span data-stu-id="b684d-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b684d-106">S2</span><span class="sxs-lookup"><span data-stu-id="b684d-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b684d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b684d-107">DESCRIPTION</span></span>
<span data-ttu-id="b684d-108">O cmdlet **Start-AzWebAppSlot** inicia um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b684d-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="b684d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b684d-109">EXAMPLES</span></span>

### <span data-ttu-id="b684d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b684d-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="b684d-111">Esse comando inicia o slot chamado Slot001 relativo ao aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="b684d-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b684d-112">OS</span><span class="sxs-lookup"><span data-stu-id="b684d-112">PARAMETERS</span></span>

### <span data-ttu-id="b684d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b684d-113">-DefaultProfile</span></span>
<span data-ttu-id="b684d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b684d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b684d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b684d-115">-Name</span></span>
<span data-ttu-id="b684d-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="b684d-116">WebApp Name</span></span>

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

### <span data-ttu-id="b684d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b684d-117">-ResourceGroupName</span></span>
<span data-ttu-id="b684d-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b684d-118">Resource Group Name</span></span>

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

### <span data-ttu-id="b684d-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="b684d-119">-Slot</span></span>
<span data-ttu-id="b684d-120">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="b684d-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="b684d-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b684d-121">-WebApp</span></span>
<span data-ttu-id="b684d-122">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="b684d-122">WebApp Object</span></span>

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

### <span data-ttu-id="b684d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b684d-123">CommonParameters</span></span>
<span data-ttu-id="b684d-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b684d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b684d-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b684d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b684d-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b684d-126">INPUTS</span></span>

### <span data-ttu-id="b684d-127">Instalação</span><span class="sxs-lookup"><span data-stu-id="b684d-127">Site</span></span>
<span data-ttu-id="b684d-128">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="b684d-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b684d-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b684d-129">OUTPUTS</span></span>

## <span data-ttu-id="b684d-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b684d-130">NOTES</span></span>

## <span data-ttu-id="b684d-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b684d-131">RELATED LINKS</span></span>

[<span data-ttu-id="b684d-132">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b684d-132">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="b684d-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b684d-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="b684d-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b684d-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="b684d-135">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b684d-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="b684d-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b684d-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="b684d-137">Parar-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b684d-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="b684d-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b684d-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
