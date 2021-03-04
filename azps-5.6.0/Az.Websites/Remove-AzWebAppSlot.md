---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: cca1cc480f529c49f679930d9d88f39f69f6e966
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889359"
---
# <span data-ttu-id="072ce-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="072ce-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="072ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="072ce-102">SYNOPSIS</span></span>

## <span data-ttu-id="072ce-103">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="072ce-103">SYNTAX</span></span>

### <span data-ttu-id="072ce-104">S1</span><span class="sxs-lookup"><span data-stu-id="072ce-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="072ce-105">S2</span><span class="sxs-lookup"><span data-stu-id="072ce-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="072ce-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="072ce-106">DESCRIPTION</span></span>
<span data-ttu-id="072ce-107">O cmdlet **Remove-AzWebAppSlot** remove um Slot do Aplicativo Web do Azure fornecido para o grupo de recursos e o nome do Aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="072ce-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="072ce-108">Esse cmdlet, por padrão, também remove todos os slots e métricas.</span><span class="sxs-lookup"><span data-stu-id="072ce-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="072ce-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="072ce-109">EXAMPLES</span></span>

### <span data-ttu-id="072ce-110">Exemplo 1: Remover um slot de aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="072ce-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="072ce-111">Este comando remove o Slot chamado Slot001 associado ao Web App ContosoSite que pertence ao grupo de recursos chamado Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="072ce-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="072ce-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="072ce-112">PARAMETERS</span></span>

### <span data-ttu-id="072ce-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="072ce-113">-AsJob</span></span>
<span data-ttu-id="072ce-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="072ce-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="072ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="072ce-115">-DefaultProfile</span></span>
<span data-ttu-id="072ce-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="072ce-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="072ce-117">-Force</span><span class="sxs-lookup"><span data-stu-id="072ce-117">-Force</span></span>
<span data-ttu-id="072ce-118">Opção Remover com força</span><span class="sxs-lookup"><span data-stu-id="072ce-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="072ce-119">-Name</span><span class="sxs-lookup"><span data-stu-id="072ce-119">-Name</span></span>
<span data-ttu-id="072ce-120">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="072ce-120">WebApp Name</span></span>

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

### <span data-ttu-id="072ce-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="072ce-121">-ResourceGroupName</span></span>
<span data-ttu-id="072ce-122">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="072ce-122">Resource Group Name</span></span>

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

### <span data-ttu-id="072ce-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="072ce-123">-Slot</span></span>
<span data-ttu-id="072ce-124">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="072ce-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="072ce-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="072ce-125">-WebApp</span></span>
<span data-ttu-id="072ce-126">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="072ce-126">WebApp Object</span></span>

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

### <span data-ttu-id="072ce-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="072ce-127">-Confirm</span></span>
<span data-ttu-id="072ce-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="072ce-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="072ce-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="072ce-129">-WhatIf</span></span>
<span data-ttu-id="072ce-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="072ce-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="072ce-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="072ce-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="072ce-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="072ce-132">CommonParameters</span></span>
<span data-ttu-id="072ce-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="072ce-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="072ce-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="072ce-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="072ce-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="072ce-135">INPUTS</span></span>

### <span data-ttu-id="072ce-136">System.String</span><span class="sxs-lookup"><span data-stu-id="072ce-136">System.String</span></span>

### <span data-ttu-id="072ce-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="072ce-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="072ce-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="072ce-138">OUTPUTS</span></span>

### <span data-ttu-id="072ce-139">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="072ce-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="072ce-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="072ce-140">NOTES</span></span>

## <span data-ttu-id="072ce-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="072ce-141">RELATED LINKS</span></span>

[<span data-ttu-id="072ce-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="072ce-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="072ce-143">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="072ce-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="072ce-144">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="072ce-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="072ce-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="072ce-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="072ce-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="072ce-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="072ce-147">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="072ce-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="072ce-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="072ce-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
