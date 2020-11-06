---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: a984a9a76a41db93bee96acfa029ca05a30d85f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428682"
---
# <span data-ttu-id="a1a98-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a1a98-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="a1a98-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1a98-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a98-103">Remove um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1a98-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1a98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1a98-104">SYNTAX</span></span>

### <span data-ttu-id="a1a98-105">Eles</span><span class="sxs-lookup"><span data-stu-id="a1a98-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1a98-106">S2</span><span class="sxs-lookup"><span data-stu-id="a1a98-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-WebApp] <Site> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1a98-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1a98-107">DESCRIPTION</span></span>
<span data-ttu-id="a1a98-108">O cmdlet **Remove-AzureRmWebApp** remove um aplicativo Web do Azure desde o grupo de recursos e o nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="a1a98-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="a1a98-109">Esse cmdlet, por padrão, também remove todos os slots e métricas.</span><span class="sxs-lookup"><span data-stu-id="a1a98-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="a1a98-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1a98-110">EXAMPLES</span></span>

### <span data-ttu-id="a1a98-111">Exemplo 1: remover um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="a1a98-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="a1a98-112">Esse comando Remove o aplicativo Web do Azure chamado ContosoSite que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="a1a98-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a1a98-113">OS</span><span class="sxs-lookup"><span data-stu-id="a1a98-113">PARAMETERS</span></span>

### <span data-ttu-id="a1a98-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a98-114">-DefaultProfile</span></span>
<span data-ttu-id="a1a98-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1a98-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a98-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a1a98-116">-Force</span></span>
<span data-ttu-id="a1a98-117">Opção de remoção forçada</span><span class="sxs-lookup"><span data-stu-id="a1a98-117">Forcefully Remove Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a98-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1a98-118">-Name</span></span>
<span data-ttu-id="a1a98-119">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="a1a98-119">WebApp Name</span></span>

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

### <span data-ttu-id="a1a98-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1a98-120">-ResourceGroupName</span></span>
<span data-ttu-id="a1a98-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a1a98-121">Resource Group Name</span></span>

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

### <span data-ttu-id="a1a98-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a1a98-122">-WebApp</span></span>
<span data-ttu-id="a1a98-123">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="a1a98-123">WebApp Object</span></span>

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

### <span data-ttu-id="a1a98-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a1a98-124">-Confirm</span></span>
<span data-ttu-id="a1a98-125">Solicita confirmação antes de executar o cmdlet. Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1a98-125">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a98-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1a98-126">-WhatIf</span></span>
<span data-ttu-id="a1a98-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1a98-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1a98-128">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1a98-128">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1a98-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1a98-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a98-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1a98-130">-AsJob</span></span>
<span data-ttu-id="a1a98-131">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a1a98-131">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a98-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a98-132">CommonParameters</span></span>
<span data-ttu-id="a1a98-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1a98-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a98-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1a98-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a98-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1a98-135">INPUTS</span></span>

### <span data-ttu-id="a1a98-136">Instalação</span><span class="sxs-lookup"><span data-stu-id="a1a98-136">Site</span></span>
<span data-ttu-id="a1a98-137">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="a1a98-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a1a98-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1a98-138">OUTPUTS</span></span>

## <span data-ttu-id="a1a98-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1a98-139">NOTES</span></span>

## <span data-ttu-id="a1a98-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1a98-140">RELATED LINKS</span></span>

[<span data-ttu-id="a1a98-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a1a98-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="a1a98-142">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a1a98-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="a1a98-143">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a1a98-143">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="a1a98-144">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a1a98-144">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="a1a98-145">Parar-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a1a98-145">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


