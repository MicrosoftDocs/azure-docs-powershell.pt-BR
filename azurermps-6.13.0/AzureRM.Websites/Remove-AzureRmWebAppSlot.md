---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 7fdf5e8de2ec326888c57e8219a006f9ef447aa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430788"
---
# <span data-ttu-id="122dc-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="122dc-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="122dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="122dc-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="122dc-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="122dc-103">SYNTAX</span></span>

### <span data-ttu-id="122dc-104">Eles</span><span class="sxs-lookup"><span data-stu-id="122dc-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="122dc-105">S2</span><span class="sxs-lookup"><span data-stu-id="122dc-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="122dc-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="122dc-106">DESCRIPTION</span></span>
<span data-ttu-id="122dc-107">O cmdlet **Remove-AzureRmWebAppSlot** remove um slot do aplicativo Web do Azure fornecido com o grupo de recursos e o nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="122dc-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="122dc-108">Esse cmdlet, por padrão, também remove todos os slots e métricas.</span><span class="sxs-lookup"><span data-stu-id="122dc-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="122dc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="122dc-109">EXAMPLES</span></span>

### <span data-ttu-id="122dc-110">Exemplo 1: remover um slot de aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="122dc-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="122dc-111">Esse comando Remove o slot nomeado Slot001 associado à ContosoSite do aplicativo Web que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="122dc-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="122dc-112">OS</span><span class="sxs-lookup"><span data-stu-id="122dc-112">PARAMETERS</span></span>

### <span data-ttu-id="122dc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="122dc-113">-AsJob</span></span>
<span data-ttu-id="122dc-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="122dc-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="122dc-115">-DefaultProfile</span></span>
<span data-ttu-id="122dc-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="122dc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="122dc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="122dc-117">-Force</span></span>
<span data-ttu-id="122dc-118">Opção de remoção forçada</span><span class="sxs-lookup"><span data-stu-id="122dc-118">Forcefully Remove Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122dc-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="122dc-119">-Name</span></span>
<span data-ttu-id="122dc-120">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="122dc-120">WebApp Name</span></span>

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

### <span data-ttu-id="122dc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="122dc-121">-ResourceGroupName</span></span>
<span data-ttu-id="122dc-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="122dc-122">Resource Group Name</span></span>

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

### <span data-ttu-id="122dc-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="122dc-123">-Slot</span></span>
<span data-ttu-id="122dc-124">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="122dc-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="122dc-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="122dc-125">-WebApp</span></span>
<span data-ttu-id="122dc-126">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="122dc-126">WebApp Object</span></span>

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

### <span data-ttu-id="122dc-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="122dc-127">-Confirm</span></span>
<span data-ttu-id="122dc-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="122dc-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122dc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="122dc-129">-WhatIf</span></span>
<span data-ttu-id="122dc-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="122dc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="122dc-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="122dc-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122dc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="122dc-132">CommonParameters</span></span>
<span data-ttu-id="122dc-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="122dc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="122dc-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="122dc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="122dc-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="122dc-135">INPUTS</span></span>

### <span data-ttu-id="122dc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="122dc-136">System.String</span></span>

### <span data-ttu-id="122dc-137">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="122dc-137">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="122dc-138">Parâmetros: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="122dc-138">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="122dc-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="122dc-139">OUTPUTS</span></span>

### <span data-ttu-id="122dc-140">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="122dc-140">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="122dc-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="122dc-141">NOTES</span></span>

## <span data-ttu-id="122dc-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="122dc-142">RELATED LINKS</span></span>

[<span data-ttu-id="122dc-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="122dc-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="122dc-144">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="122dc-144">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="122dc-145">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="122dc-145">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="122dc-146">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="122dc-146">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="122dc-147">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="122dc-147">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="122dc-148">Parar-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="122dc-148">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="122dc-149">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="122dc-149">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
