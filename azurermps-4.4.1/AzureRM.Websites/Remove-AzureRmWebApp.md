---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: b903e22a627ca2cb992b179e8f6956d556558b6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440914"
---
# <span data-ttu-id="68b73-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="68b73-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="68b73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="68b73-102">SYNOPSIS</span></span>
<span data-ttu-id="68b73-103">Remove um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="68b73-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68b73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68b73-104">SYNTAX</span></span>

### <span data-ttu-id="68b73-105">Eles</span><span class="sxs-lookup"><span data-stu-id="68b73-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68b73-106">S2</span><span class="sxs-lookup"><span data-stu-id="68b73-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68b73-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="68b73-107">DESCRIPTION</span></span>
<span data-ttu-id="68b73-108">O cmdlet **Remove-AzureRmWebApp** remove um aplicativo Web do Azure desde o grupo de recursos e o nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="68b73-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="68b73-109">Esse cmdlet, por padrão, também remove todos os slots e métricas.</span><span class="sxs-lookup"><span data-stu-id="68b73-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="68b73-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68b73-110">EXAMPLES</span></span>

### <span data-ttu-id="68b73-111">Exemplo 1: remover um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="68b73-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="68b73-112">Esse comando Remove o aplicativo Web do Azure chamado ContosoSite que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="68b73-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="68b73-113">OS</span><span class="sxs-lookup"><span data-stu-id="68b73-113">PARAMETERS</span></span>

### <span data-ttu-id="68b73-114">-Force</span><span class="sxs-lookup"><span data-stu-id="68b73-114">-Force</span></span>
<span data-ttu-id="68b73-115">Opção de remoção forçada</span><span class="sxs-lookup"><span data-stu-id="68b73-115">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="68b73-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="68b73-116">-Name</span></span>
<span data-ttu-id="68b73-117">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="68b73-117">WebApp Name</span></span>

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

### <span data-ttu-id="68b73-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68b73-118">-ResourceGroupName</span></span>
<span data-ttu-id="68b73-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="68b73-119">Resource Group Name</span></span>

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

### <span data-ttu-id="68b73-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="68b73-120">-WebApp</span></span>
<span data-ttu-id="68b73-121">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="68b73-121">WebApp Object</span></span>

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

### <span data-ttu-id="68b73-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="68b73-122">-Confirm</span></span>
<span data-ttu-id="68b73-123">Solicita confirmação antes de executar o cmdlet. Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68b73-123">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68b73-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68b73-124">-WhatIf</span></span>
<span data-ttu-id="68b73-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="68b73-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68b73-126">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="68b73-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68b73-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="68b73-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68b73-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68b73-128">-DefaultProfile</span></span>
<span data-ttu-id="68b73-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="68b73-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68b73-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68b73-130">CommonParameters</span></span>
<span data-ttu-id="68b73-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68b73-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68b73-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68b73-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68b73-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="68b73-133">INPUTS</span></span>

### <span data-ttu-id="68b73-134">Instalação</span><span class="sxs-lookup"><span data-stu-id="68b73-134">Site</span></span>
<span data-ttu-id="68b73-135">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="68b73-135">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="68b73-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="68b73-136">OUTPUTS</span></span>

## <span data-ttu-id="68b73-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="68b73-137">NOTES</span></span>

## <span data-ttu-id="68b73-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68b73-138">RELATED LINKS</span></span>

[<span data-ttu-id="68b73-139">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="68b73-139">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="68b73-140">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="68b73-140">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="68b73-141">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="68b73-141">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="68b73-142">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="68b73-142">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="68b73-143">Parar-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="68b73-143">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


