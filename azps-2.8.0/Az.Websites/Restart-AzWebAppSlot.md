---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 53323aaf29145f4340dd00fa752d8afd2dd72131
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774372"
---
# <span data-ttu-id="6c17e-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6c17e-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="6c17e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c17e-102">SYNOPSIS</span></span>

## <span data-ttu-id="6c17e-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c17e-103">SYNTAX</span></span>

### <span data-ttu-id="6c17e-104">Eles</span><span class="sxs-lookup"><span data-stu-id="6c17e-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c17e-105">S2</span><span class="sxs-lookup"><span data-stu-id="6c17e-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c17e-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6c17e-106">DESCRIPTION</span></span>
<span data-ttu-id="6c17e-107">O cmdlet **Restart-AzWebAppSlot** interrompe e, em seguida, inicia um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="6c17e-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="6c17e-108">Se o slot do aplicativo Web estiver em um estado parado, use o cmdlet Start-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="6c17e-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="6c17e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c17e-109">EXAMPLES</span></span>

### <span data-ttu-id="6c17e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6c17e-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="6c17e-111">Esse comando reinicia o slot Slot001 para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="6c17e-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="6c17e-112">OS</span><span class="sxs-lookup"><span data-stu-id="6c17e-112">PARAMETERS</span></span>

### <span data-ttu-id="6c17e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c17e-113">-DefaultProfile</span></span>
<span data-ttu-id="6c17e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6c17e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c17e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c17e-115">-Name</span></span>
<span data-ttu-id="6c17e-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="6c17e-116">WebApp Name</span></span>

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

### <span data-ttu-id="6c17e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c17e-117">-ResourceGroupName</span></span>
<span data-ttu-id="6c17e-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6c17e-118">Resource Group Name</span></span>

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

### <span data-ttu-id="6c17e-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="6c17e-119">-Slot</span></span>
<span data-ttu-id="6c17e-120">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="6c17e-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="6c17e-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6c17e-121">-WebApp</span></span>
<span data-ttu-id="6c17e-122">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="6c17e-122">WebApp Object</span></span>

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

### <span data-ttu-id="6c17e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c17e-123">CommonParameters</span></span>
<span data-ttu-id="6c17e-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c17e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c17e-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c17e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c17e-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6c17e-126">INPUTS</span></span>

### <span data-ttu-id="6c17e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6c17e-127">System.String</span></span>

### <span data-ttu-id="6c17e-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="6c17e-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6c17e-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6c17e-129">OUTPUTS</span></span>

### <span data-ttu-id="6c17e-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="6c17e-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6c17e-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6c17e-131">NOTES</span></span>

## <span data-ttu-id="6c17e-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c17e-132">RELATED LINKS</span></span>

[<span data-ttu-id="6c17e-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6c17e-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="6c17e-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6c17e-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="6c17e-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6c17e-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="6c17e-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6c17e-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="6c17e-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6c17e-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="6c17e-138">Parar-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6c17e-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="6c17e-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6c17e-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
