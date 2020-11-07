---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: c91e5ff71a916e28e199a1c64fde2d69f0193fd1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774441"
---
# <span data-ttu-id="06512-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="06512-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="06512-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06512-102">SYNOPSIS</span></span>
<span data-ttu-id="06512-103">Remove um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="06512-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="06512-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06512-104">SYNTAX</span></span>

### <span data-ttu-id="06512-105">Eles</span><span class="sxs-lookup"><span data-stu-id="06512-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06512-106">S2</span><span class="sxs-lookup"><span data-stu-id="06512-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06512-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06512-107">DESCRIPTION</span></span>
<span data-ttu-id="06512-108">O cmdlet **Remove-AzWebApp** remove um aplicativo Web do Azure desde o grupo de recursos e o nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="06512-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="06512-109">Esse cmdlet, por padrão, também remove todos os slots e métricas.</span><span class="sxs-lookup"><span data-stu-id="06512-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="06512-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06512-110">EXAMPLES</span></span>

### <span data-ttu-id="06512-111">Exemplo 1: remover um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="06512-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="06512-112">Esse comando Remove o aplicativo Web do Azure chamado ContosoSite que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="06512-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="06512-113">OS</span><span class="sxs-lookup"><span data-stu-id="06512-113">PARAMETERS</span></span>

### <span data-ttu-id="06512-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06512-114">-AsJob</span></span>
<span data-ttu-id="06512-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="06512-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06512-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06512-116">-DefaultProfile</span></span>
<span data-ttu-id="06512-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06512-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06512-118">-Force</span><span class="sxs-lookup"><span data-stu-id="06512-118">-Force</span></span>
<span data-ttu-id="06512-119">Opção de remoção forçada</span><span class="sxs-lookup"><span data-stu-id="06512-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="06512-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="06512-120">-Name</span></span>
<span data-ttu-id="06512-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="06512-121">WebApp Name</span></span>

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

### <span data-ttu-id="06512-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06512-122">-ResourceGroupName</span></span>
<span data-ttu-id="06512-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="06512-123">Resource Group Name</span></span>

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

### <span data-ttu-id="06512-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="06512-124">-WebApp</span></span>
<span data-ttu-id="06512-125">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="06512-125">WebApp Object</span></span>

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

### <span data-ttu-id="06512-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="06512-126">-Confirm</span></span>
<span data-ttu-id="06512-127">Solicita confirmação antes de executar o cmdlet. Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06512-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06512-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06512-128">-WhatIf</span></span>
<span data-ttu-id="06512-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="06512-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06512-130">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="06512-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06512-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="06512-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06512-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06512-132">CommonParameters</span></span>
<span data-ttu-id="06512-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06512-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06512-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06512-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06512-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06512-135">INPUTS</span></span>

### <span data-ttu-id="06512-136">System. String</span><span class="sxs-lookup"><span data-stu-id="06512-136">System.String</span></span>

### <span data-ttu-id="06512-137">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="06512-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="06512-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06512-138">OUTPUTS</span></span>

### <span data-ttu-id="06512-139">System. void</span><span class="sxs-lookup"><span data-stu-id="06512-139">System.Void</span></span>

## <span data-ttu-id="06512-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06512-140">NOTES</span></span>

## <span data-ttu-id="06512-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06512-141">RELATED LINKS</span></span>

[<span data-ttu-id="06512-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="06512-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="06512-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="06512-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="06512-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="06512-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="06512-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="06512-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="06512-146">Parar-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="06512-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


