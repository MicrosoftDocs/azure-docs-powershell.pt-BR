---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118505"
---
# <span data-ttu-id="4d974-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d974-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="4d974-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d974-102">SYNOPSIS</span></span>
<span data-ttu-id="4d974-103">Obtém um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="4d974-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="4d974-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d974-104">SYNTAX</span></span>

### <span data-ttu-id="4d974-105">S1</span><span class="sxs-lookup"><span data-stu-id="4d974-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d974-106">S2</span><span class="sxs-lookup"><span data-stu-id="4d974-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d974-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d974-107">DESCRIPTION</span></span>
<span data-ttu-id="4d974-108">O **cmdlet Get-AzWebAppSlot** obtém informações sobre um Slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="4d974-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="4d974-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4d974-109">EXAMPLES</span></span>

### <span data-ttu-id="4d974-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4d974-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="4d974-111">Esse comando obtém o slot chamado Slot001 do Web App chamado WebAppStandard que pertence ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="4d974-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="4d974-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d974-112">PARAMETERS</span></span>

### <span data-ttu-id="4d974-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d974-113">-DefaultProfile</span></span>
<span data-ttu-id="4d974-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4d974-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d974-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d974-115">-Name</span></span>
<span data-ttu-id="4d974-116">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="4d974-116">WebApp Name</span></span>

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

### <span data-ttu-id="4d974-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d974-117">-ResourceGroupName</span></span>
<span data-ttu-id="4d974-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="4d974-118">Resource Group Name</span></span>

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

### <span data-ttu-id="4d974-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="4d974-119">-Slot</span></span>
<span data-ttu-id="4d974-120">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="4d974-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="4d974-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4d974-121">-WebApp</span></span>
<span data-ttu-id="4d974-122">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="4d974-122">WebApp Object</span></span>

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

### <span data-ttu-id="4d974-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d974-123">CommonParameters</span></span>
<span data-ttu-id="4d974-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d974-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d974-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d974-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d974-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="4d974-126">INPUTS</span></span>

### <span data-ttu-id="4d974-127">System.String</span><span class="sxs-lookup"><span data-stu-id="4d974-127">System.String</span></span>

### <span data-ttu-id="4d974-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="4d974-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4d974-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="4d974-129">OUTPUTS</span></span>

### <span data-ttu-id="4d974-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="4d974-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4d974-131">Notas</span><span class="sxs-lookup"><span data-stu-id="4d974-131">NOTES</span></span>

## <span data-ttu-id="4d974-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d974-132">RELATED LINKS</span></span>

[<span data-ttu-id="4d974-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d974-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="4d974-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d974-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="4d974-135">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d974-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="4d974-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d974-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="4d974-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d974-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="4d974-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d974-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="4d974-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4d974-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
