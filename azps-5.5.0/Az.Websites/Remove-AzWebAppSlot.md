---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 88eaf66ea8584913c7816fd12be19509aec49de5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118843"
---
# <span data-ttu-id="8ea25-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8ea25-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="8ea25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ea25-102">SYNOPSIS</span></span>

## <span data-ttu-id="8ea25-103">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ea25-103">SYNTAX</span></span>

### <span data-ttu-id="8ea25-104">S1</span><span class="sxs-lookup"><span data-stu-id="8ea25-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ea25-105">S2</span><span class="sxs-lookup"><span data-stu-id="8ea25-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ea25-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ea25-106">DESCRIPTION</span></span>
<span data-ttu-id="8ea25-107">O cmdlet **Remove-AzWebAppSlot** remove um Slot do Azure Web App fornecido ao grupo de recursos e ao nome do Web App.</span><span class="sxs-lookup"><span data-stu-id="8ea25-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="8ea25-108">Esse cmdlet, por padrão, também remove todos os slots e métricas.</span><span class="sxs-lookup"><span data-stu-id="8ea25-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="8ea25-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8ea25-109">EXAMPLES</span></span>

### <span data-ttu-id="8ea25-110">Exemplo 1: Remover um Slot do Web App</span><span class="sxs-lookup"><span data-stu-id="8ea25-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="8ea25-111">Esse comando remove o Slot chamado Slot001 associado ao Web App ContosoSite que pertence ao grupo de recursos chamado Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="8ea25-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="8ea25-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ea25-112">PARAMETERS</span></span>

### <span data-ttu-id="8ea25-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ea25-113">-AsJob</span></span>
<span data-ttu-id="8ea25-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8ea25-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ea25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ea25-115">-DefaultProfile</span></span>
<span data-ttu-id="8ea25-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8ea25-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ea25-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="8ea25-117">-Force</span></span>
<span data-ttu-id="8ea25-118">Opção Remover Com Força</span><span class="sxs-lookup"><span data-stu-id="8ea25-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="8ea25-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ea25-119">-Name</span></span>
<span data-ttu-id="8ea25-120">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="8ea25-120">WebApp Name</span></span>

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

### <span data-ttu-id="8ea25-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ea25-121">-ResourceGroupName</span></span>
<span data-ttu-id="8ea25-122">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="8ea25-122">Resource Group Name</span></span>

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

### <span data-ttu-id="8ea25-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="8ea25-123">-Slot</span></span>
<span data-ttu-id="8ea25-124">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="8ea25-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8ea25-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8ea25-125">-WebApp</span></span>
<span data-ttu-id="8ea25-126">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="8ea25-126">WebApp Object</span></span>

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

### <span data-ttu-id="8ea25-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8ea25-127">-Confirm</span></span>
<span data-ttu-id="8ea25-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ea25-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ea25-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ea25-129">-WhatIf</span></span>
<span data-ttu-id="8ea25-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8ea25-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ea25-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8ea25-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ea25-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ea25-132">CommonParameters</span></span>
<span data-ttu-id="8ea25-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ea25-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ea25-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ea25-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ea25-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="8ea25-135">INPUTS</span></span>

### <span data-ttu-id="8ea25-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8ea25-136">System.String</span></span>

### <span data-ttu-id="8ea25-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8ea25-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8ea25-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="8ea25-138">OUTPUTS</span></span>

### <span data-ttu-id="8ea25-139">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8ea25-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="8ea25-140">Notas</span><span class="sxs-lookup"><span data-stu-id="8ea25-140">NOTES</span></span>

## <span data-ttu-id="8ea25-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ea25-141">RELATED LINKS</span></span>

[<span data-ttu-id="8ea25-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8ea25-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="8ea25-143">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8ea25-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="8ea25-144">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8ea25-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="8ea25-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8ea25-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="8ea25-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8ea25-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="8ea25-147">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8ea25-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="8ea25-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8ea25-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
