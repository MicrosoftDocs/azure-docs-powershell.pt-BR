---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 64d463e6cbe3012b8d49e0a61b4f081f286e25b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112328"
---
# <span data-ttu-id="2cb39-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2cb39-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="2cb39-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2cb39-102">SYNOPSIS</span></span>
<span data-ttu-id="2cb39-103">Remove um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="2cb39-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="2cb39-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2cb39-104">SYNTAX</span></span>

### <span data-ttu-id="2cb39-105">S1</span><span class="sxs-lookup"><span data-stu-id="2cb39-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cb39-106">S2</span><span class="sxs-lookup"><span data-stu-id="2cb39-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cb39-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2cb39-107">DESCRIPTION</span></span>
<span data-ttu-id="2cb39-108">O cmdlet **Remove-AzWebApp** remove um Azure Web App fornecido ao grupo de recursos e ao nome do Web App.</span><span class="sxs-lookup"><span data-stu-id="2cb39-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="2cb39-109">Esse cmdlet, por padrão, também remove todos os slots e métricas.</span><span class="sxs-lookup"><span data-stu-id="2cb39-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="2cb39-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2cb39-110">EXAMPLES</span></span>

### <span data-ttu-id="2cb39-111">Exemplo 1: Remover um Aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="2cb39-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="2cb39-112">Esse comando remove o Azure Web App chamado ContosoSite que pertence ao grupo de recursos chamado Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="2cb39-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="2cb39-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2cb39-113">PARAMETERS</span></span>

### <span data-ttu-id="2cb39-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cb39-114">-AsJob</span></span>
<span data-ttu-id="2cb39-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2cb39-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2cb39-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cb39-116">-DefaultProfile</span></span>
<span data-ttu-id="2cb39-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2cb39-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cb39-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="2cb39-118">-Force</span></span>
<span data-ttu-id="2cb39-119">Opção Remover Com Força</span><span class="sxs-lookup"><span data-stu-id="2cb39-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="2cb39-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2cb39-120">-Name</span></span>
<span data-ttu-id="2cb39-121">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="2cb39-121">WebApp Name</span></span>

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

### <span data-ttu-id="2cb39-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cb39-122">-ResourceGroupName</span></span>
<span data-ttu-id="2cb39-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="2cb39-123">Resource Group Name</span></span>

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

### <span data-ttu-id="2cb39-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2cb39-124">-WebApp</span></span>
<span data-ttu-id="2cb39-125">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="2cb39-125">WebApp Object</span></span>

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

### <span data-ttu-id="2cb39-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2cb39-126">-Confirm</span></span>
<span data-ttu-id="2cb39-127">Solicita confirmação antes de executar o cmdlet. Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cb39-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cb39-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cb39-128">-WhatIf</span></span>
<span data-ttu-id="2cb39-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2cb39-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cb39-130">O cmdlet não é executado. Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2cb39-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cb39-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2cb39-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cb39-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cb39-132">CommonParameters</span></span>
<span data-ttu-id="2cb39-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cb39-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cb39-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cb39-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cb39-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="2cb39-135">INPUTS</span></span>

### <span data-ttu-id="2cb39-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2cb39-136">System.String</span></span>

### <span data-ttu-id="2cb39-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="2cb39-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2cb39-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="2cb39-138">OUTPUTS</span></span>

### <span data-ttu-id="2cb39-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="2cb39-139">System.Void</span></span>

## <span data-ttu-id="2cb39-140">Notas</span><span class="sxs-lookup"><span data-stu-id="2cb39-140">NOTES</span></span>

## <span data-ttu-id="2cb39-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2cb39-141">RELATED LINKS</span></span>

[<span data-ttu-id="2cb39-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2cb39-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="2cb39-143">Novo-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2cb39-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="2cb39-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2cb39-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="2cb39-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2cb39-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="2cb39-146">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2cb39-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


