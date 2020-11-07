---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 377e08f344256f6d744fec66f0b6b20f495d9309
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942913"
---
# <span data-ttu-id="71683-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71683-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="71683-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71683-102">SYNOPSIS</span></span>

## <span data-ttu-id="71683-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71683-103">SYNTAX</span></span>

### <span data-ttu-id="71683-104">Eles</span><span class="sxs-lookup"><span data-stu-id="71683-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71683-105">S2</span><span class="sxs-lookup"><span data-stu-id="71683-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71683-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71683-106">DESCRIPTION</span></span>
<span data-ttu-id="71683-107">O cmdlet **Restart-AzWebAppSlot** interrompe e, em seguida, inicia um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="71683-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="71683-108">Se o slot do aplicativo Web estiver em um estado parado, use o cmdlet Start-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="71683-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="71683-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71683-109">EXAMPLES</span></span>

### <span data-ttu-id="71683-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="71683-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="71683-111">Esse comando reinicia o slot Slot001 para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="71683-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="71683-112">OS</span><span class="sxs-lookup"><span data-stu-id="71683-112">PARAMETERS</span></span>

### <span data-ttu-id="71683-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71683-113">-DefaultProfile</span></span>
<span data-ttu-id="71683-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71683-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71683-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="71683-115">-Name</span></span>
<span data-ttu-id="71683-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="71683-116">WebApp Name</span></span>

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

### <span data-ttu-id="71683-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71683-117">-ResourceGroupName</span></span>
<span data-ttu-id="71683-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="71683-118">Resource Group Name</span></span>

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

### <span data-ttu-id="71683-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="71683-119">-Slot</span></span>
<span data-ttu-id="71683-120">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="71683-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="71683-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="71683-121">-WebApp</span></span>
<span data-ttu-id="71683-122">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="71683-122">WebApp Object</span></span>

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

### <span data-ttu-id="71683-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71683-123">CommonParameters</span></span>
<span data-ttu-id="71683-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71683-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71683-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71683-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71683-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71683-126">INPUTS</span></span>

### <span data-ttu-id="71683-127">System. String</span><span class="sxs-lookup"><span data-stu-id="71683-127">System.String</span></span>

### <span data-ttu-id="71683-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="71683-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="71683-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71683-129">OUTPUTS</span></span>

### <span data-ttu-id="71683-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="71683-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="71683-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71683-131">NOTES</span></span>

## <span data-ttu-id="71683-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71683-132">RELATED LINKS</span></span>

[<span data-ttu-id="71683-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71683-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="71683-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71683-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="71683-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71683-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="71683-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71683-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="71683-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71683-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="71683-138">Parar-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71683-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="71683-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="71683-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
