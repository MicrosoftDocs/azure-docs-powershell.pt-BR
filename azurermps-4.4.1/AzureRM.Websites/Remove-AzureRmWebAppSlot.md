---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 65393bc3dd2e9e6b51699a21baf0e6d3750464bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440911"
---
# <span data-ttu-id="6de94-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6de94-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="6de94-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6de94-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6de94-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6de94-103">SYNTAX</span></span>

### <span data-ttu-id="6de94-104">Eles</span><span class="sxs-lookup"><span data-stu-id="6de94-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6de94-105">S2</span><span class="sxs-lookup"><span data-stu-id="6de94-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6de94-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6de94-106">DESCRIPTION</span></span>
<span data-ttu-id="6de94-107">O cmdlet **Remove-AzureRmWebAppSlot** remove um slot do aplicativo Web do Azure fornecido com o grupo de recursos e o nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="6de94-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="6de94-108">Esse cmdlet, por padrão, também remove todos os slots e métricas.</span><span class="sxs-lookup"><span data-stu-id="6de94-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="6de94-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6de94-109">EXAMPLES</span></span>

### <span data-ttu-id="6de94-110">Exemplo 1: remover um slot de aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="6de94-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="6de94-111">Esse comando Remove o slot nomeado Slot001 associado à ContosoSite do aplicativo Web que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="6de94-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="6de94-112">OS</span><span class="sxs-lookup"><span data-stu-id="6de94-112">PARAMETERS</span></span>

### <span data-ttu-id="6de94-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6de94-113">-Force</span></span>
<span data-ttu-id="6de94-114">Opção de remoção forçada</span><span class="sxs-lookup"><span data-stu-id="6de94-114">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="6de94-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6de94-115">-Name</span></span>
<span data-ttu-id="6de94-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="6de94-116">WebApp Name</span></span>

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

### <span data-ttu-id="6de94-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6de94-117">-ResourceGroupName</span></span>
<span data-ttu-id="6de94-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6de94-118">Resource Group Name</span></span>

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

### <span data-ttu-id="6de94-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="6de94-119">-Slot</span></span>
<span data-ttu-id="6de94-120">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="6de94-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="6de94-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6de94-121">-WebApp</span></span>
<span data-ttu-id="6de94-122">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="6de94-122">WebApp Object</span></span>

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

### <span data-ttu-id="6de94-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6de94-123">-Confirm</span></span>
<span data-ttu-id="6de94-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6de94-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6de94-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6de94-125">-WhatIf</span></span>
<span data-ttu-id="6de94-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6de94-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6de94-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6de94-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6de94-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de94-128">-DefaultProfile</span></span>
<span data-ttu-id="6de94-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6de94-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6de94-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de94-130">CommonParameters</span></span>
<span data-ttu-id="6de94-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de94-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de94-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6de94-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de94-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6de94-133">INPUTS</span></span>

### <span data-ttu-id="6de94-134">Instalação</span><span class="sxs-lookup"><span data-stu-id="6de94-134">Site</span></span>
<span data-ttu-id="6de94-135">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="6de94-135">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6de94-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6de94-136">OUTPUTS</span></span>

### <span data-ttu-id="6de94-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6de94-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="6de94-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6de94-138">NOTES</span></span>

## <span data-ttu-id="6de94-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6de94-139">RELATED LINKS</span></span>

[<span data-ttu-id="6de94-140">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6de94-140">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="6de94-141">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6de94-141">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="6de94-142">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6de94-142">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="6de94-143">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6de94-143">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="6de94-144">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6de94-144">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="6de94-145">Parar-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6de94-145">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="6de94-146">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6de94-146">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
