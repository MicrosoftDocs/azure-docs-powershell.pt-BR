---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restart-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 9f0e48b20d19113290784d65b6bc78531dc7b2a1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776065"
---
# <span data-ttu-id="fc209-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fc209-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="fc209-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc209-102">SYNOPSIS</span></span>

## <span data-ttu-id="fc209-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc209-103">SYNTAX</span></span>

### <span data-ttu-id="fc209-104">Eles</span><span class="sxs-lookup"><span data-stu-id="fc209-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc209-105">S2</span><span class="sxs-lookup"><span data-stu-id="fc209-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc209-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc209-106">DESCRIPTION</span></span>
<span data-ttu-id="fc209-107">O cmdlet **Restart-AzWebAppSlot** interrompe e, em seguida, inicia um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="fc209-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="fc209-108">Se o slot do aplicativo Web estiver em um estado parado, use o cmdlet Start-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="fc209-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="fc209-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc209-109">EXAMPLES</span></span>

### <span data-ttu-id="fc209-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fc209-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="fc209-111">Esse comando reinicia o slot Slot001 para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="fc209-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="fc209-112">OS</span><span class="sxs-lookup"><span data-stu-id="fc209-112">PARAMETERS</span></span>

### <span data-ttu-id="fc209-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc209-113">-DefaultProfile</span></span>
<span data-ttu-id="fc209-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc209-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc209-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc209-115">-Name</span></span>
<span data-ttu-id="fc209-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="fc209-116">WebApp Name</span></span>

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

### <span data-ttu-id="fc209-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc209-117">-ResourceGroupName</span></span>
<span data-ttu-id="fc209-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fc209-118">Resource Group Name</span></span>

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

### <span data-ttu-id="fc209-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="fc209-119">-Slot</span></span>
<span data-ttu-id="fc209-120">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="fc209-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="fc209-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fc209-121">-WebApp</span></span>
<span data-ttu-id="fc209-122">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="fc209-122">WebApp Object</span></span>

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

### <span data-ttu-id="fc209-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc209-123">CommonParameters</span></span>
<span data-ttu-id="fc209-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc209-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc209-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc209-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc209-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc209-126">INPUTS</span></span>

### <span data-ttu-id="fc209-127">Instalação</span><span class="sxs-lookup"><span data-stu-id="fc209-127">Site</span></span>
<span data-ttu-id="fc209-128">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="fc209-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="fc209-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc209-129">OUTPUTS</span></span>

## <span data-ttu-id="fc209-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc209-130">NOTES</span></span>

## <span data-ttu-id="fc209-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc209-131">RELATED LINKS</span></span>

[<span data-ttu-id="fc209-132">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fc209-132">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="fc209-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fc209-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="fc209-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fc209-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="fc209-135">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fc209-135">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="fc209-136">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fc209-136">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="fc209-137">Parar-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fc209-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="fc209-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="fc209-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
