---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115735"
---
# <span data-ttu-id="18e07-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="18e07-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="18e07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18e07-102">SYNOPSIS</span></span>
<span data-ttu-id="18e07-103">Obtém um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="18e07-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="18e07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18e07-104">SYNTAX</span></span>

### <span data-ttu-id="18e07-105">Eles</span><span class="sxs-lookup"><span data-stu-id="18e07-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18e07-106">S2</span><span class="sxs-lookup"><span data-stu-id="18e07-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18e07-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18e07-107">DESCRIPTION</span></span>
<span data-ttu-id="18e07-108">O cmdlet **Get-AzWebAppSlot** Obtém informações sobre um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="18e07-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="18e07-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18e07-109">EXAMPLES</span></span>

### <span data-ttu-id="18e07-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="18e07-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="18e07-111">Esse comando obtém o slot chamado Slot001 do aplicativo Web nomeado WebAppStandard que pertence ao grupo de recursos padrão-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="18e07-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="18e07-112">OS</span><span class="sxs-lookup"><span data-stu-id="18e07-112">PARAMETERS</span></span>

### <span data-ttu-id="18e07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18e07-113">-DefaultProfile</span></span>
<span data-ttu-id="18e07-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18e07-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18e07-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="18e07-115">-Name</span></span>
<span data-ttu-id="18e07-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="18e07-116">WebApp Name</span></span>

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

### <span data-ttu-id="18e07-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18e07-117">-ResourceGroupName</span></span>
<span data-ttu-id="18e07-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="18e07-118">Resource Group Name</span></span>

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

### <span data-ttu-id="18e07-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="18e07-119">-Slot</span></span>
<span data-ttu-id="18e07-120">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="18e07-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="18e07-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="18e07-121">-WebApp</span></span>
<span data-ttu-id="18e07-122">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="18e07-122">WebApp Object</span></span>

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

### <span data-ttu-id="18e07-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18e07-123">CommonParameters</span></span>
<span data-ttu-id="18e07-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18e07-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18e07-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18e07-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18e07-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18e07-126">INPUTS</span></span>

### <span data-ttu-id="18e07-127">System. String</span><span class="sxs-lookup"><span data-stu-id="18e07-127">System.String</span></span>

### <span data-ttu-id="18e07-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="18e07-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="18e07-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18e07-129">OUTPUTS</span></span>

### <span data-ttu-id="18e07-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="18e07-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="18e07-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18e07-131">NOTES</span></span>

## <span data-ttu-id="18e07-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18e07-132">RELATED LINKS</span></span>

[<span data-ttu-id="18e07-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="18e07-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="18e07-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="18e07-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="18e07-135">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="18e07-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="18e07-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="18e07-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="18e07-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="18e07-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="18e07-138">Parar-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="18e07-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="18e07-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="18e07-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
