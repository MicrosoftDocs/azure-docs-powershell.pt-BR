---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 40b14128ec2a1dc48cf098a2c0427728c34c7e22
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776086"
---
# <span data-ttu-id="d523f-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d523f-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="d523f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d523f-102">SYNOPSIS</span></span>
<span data-ttu-id="d523f-103">Remove um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="d523f-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="d523f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d523f-104">SYNTAX</span></span>

### <span data-ttu-id="d523f-105">Eles</span><span class="sxs-lookup"><span data-stu-id="d523f-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d523f-106">S2</span><span class="sxs-lookup"><span data-stu-id="d523f-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-WebApp] <Site> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d523f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d523f-107">DESCRIPTION</span></span>
<span data-ttu-id="d523f-108">O cmdlet **Remove-AzWebApp** remove um aplicativo Web do Azure desde o grupo de recursos e o nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="d523f-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="d523f-109">Esse cmdlet, por padrão, também remove todos os slots e métricas.</span><span class="sxs-lookup"><span data-stu-id="d523f-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="d523f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d523f-110">EXAMPLES</span></span>

### <span data-ttu-id="d523f-111">Exemplo 1: remover um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="d523f-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="d523f-112">Esse comando Remove o aplicativo Web do Azure chamado ContosoSite que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="d523f-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d523f-113">OS</span><span class="sxs-lookup"><span data-stu-id="d523f-113">PARAMETERS</span></span>

### <span data-ttu-id="d523f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d523f-114">-DefaultProfile</span></span>
<span data-ttu-id="d523f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d523f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d523f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d523f-116">-Force</span></span>
<span data-ttu-id="d523f-117">Opção de remoção forçada</span><span class="sxs-lookup"><span data-stu-id="d523f-117">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="d523f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d523f-118">-Name</span></span>
<span data-ttu-id="d523f-119">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="d523f-119">WebApp Name</span></span>

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

### <span data-ttu-id="d523f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d523f-120">-ResourceGroupName</span></span>
<span data-ttu-id="d523f-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d523f-121">Resource Group Name</span></span>

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

### <span data-ttu-id="d523f-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d523f-122">-WebApp</span></span>
<span data-ttu-id="d523f-123">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="d523f-123">WebApp Object</span></span>

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

### <span data-ttu-id="d523f-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d523f-124">-Confirm</span></span>
<span data-ttu-id="d523f-125">Solicita confirmação antes de executar o cmdlet. Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d523f-125">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d523f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d523f-126">-WhatIf</span></span>
<span data-ttu-id="d523f-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d523f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d523f-128">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d523f-128">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d523f-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d523f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d523f-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d523f-130">-AsJob</span></span>
<span data-ttu-id="d523f-131">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d523f-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d523f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d523f-132">CommonParameters</span></span>
<span data-ttu-id="d523f-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d523f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d523f-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d523f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d523f-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d523f-135">INPUTS</span></span>

### <span data-ttu-id="d523f-136">Instalação</span><span class="sxs-lookup"><span data-stu-id="d523f-136">Site</span></span>
<span data-ttu-id="d523f-137">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="d523f-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d523f-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d523f-138">OUTPUTS</span></span>

## <span data-ttu-id="d523f-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d523f-139">NOTES</span></span>

## <span data-ttu-id="d523f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d523f-140">RELATED LINKS</span></span>

[<span data-ttu-id="d523f-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d523f-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="d523f-142">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d523f-142">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="d523f-143">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d523f-143">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="d523f-144">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d523f-144">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="d523f-145">Parar-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d523f-145">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


