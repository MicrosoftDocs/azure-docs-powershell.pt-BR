---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 38b11543140a0f789674e4109db8cc73c7843f02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774080"
---
# <span data-ttu-id="3dfbc-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3dfbc-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="3dfbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3dfbc-102">SYNOPSIS</span></span>

## <span data-ttu-id="3dfbc-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3dfbc-103">SYNTAX</span></span>

### <span data-ttu-id="3dfbc-104">Eles</span><span class="sxs-lookup"><span data-stu-id="3dfbc-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dfbc-105">S2</span><span class="sxs-lookup"><span data-stu-id="3dfbc-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dfbc-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3dfbc-106">DESCRIPTION</span></span>
<span data-ttu-id="3dfbc-107">O cmdlet **Remove-AzWebAppSlot** remove um slot do aplicativo Web do Azure fornecido com o grupo de recursos e o nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="3dfbc-108">Esse cmdlet, por padrão, também remove todos os slots e métricas.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="3dfbc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3dfbc-109">EXAMPLES</span></span>

### <span data-ttu-id="3dfbc-110">Exemplo 1: remover um slot de aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="3dfbc-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="3dfbc-111">Esse comando Remove o slot nomeado Slot001 associado à ContosoSite do aplicativo Web que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="3dfbc-112">OS</span><span class="sxs-lookup"><span data-stu-id="3dfbc-112">PARAMETERS</span></span>

### <span data-ttu-id="3dfbc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3dfbc-113">-AsJob</span></span>
<span data-ttu-id="3dfbc-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3dfbc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3dfbc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dfbc-115">-DefaultProfile</span></span>
<span data-ttu-id="3dfbc-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dfbc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3dfbc-117">-Force</span></span>
<span data-ttu-id="3dfbc-118">Opção de remoção forçada</span><span class="sxs-lookup"><span data-stu-id="3dfbc-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="3dfbc-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="3dfbc-119">-Name</span></span>
<span data-ttu-id="3dfbc-120">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="3dfbc-120">WebApp Name</span></span>

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

### <span data-ttu-id="3dfbc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dfbc-121">-ResourceGroupName</span></span>
<span data-ttu-id="3dfbc-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3dfbc-122">Resource Group Name</span></span>

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

### <span data-ttu-id="3dfbc-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="3dfbc-123">-Slot</span></span>
<span data-ttu-id="3dfbc-124">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="3dfbc-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="3dfbc-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3dfbc-125">-WebApp</span></span>
<span data-ttu-id="3dfbc-126">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="3dfbc-126">WebApp Object</span></span>

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

### <span data-ttu-id="3dfbc-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3dfbc-127">-Confirm</span></span>
<span data-ttu-id="3dfbc-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dfbc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dfbc-129">-WhatIf</span></span>
<span data-ttu-id="3dfbc-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dfbc-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dfbc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dfbc-132">CommonParameters</span></span>
<span data-ttu-id="3dfbc-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dfbc-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dfbc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dfbc-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3dfbc-135">INPUTS</span></span>

### <span data-ttu-id="3dfbc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3dfbc-136">System.String</span></span>

### <span data-ttu-id="3dfbc-137">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="3dfbc-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3dfbc-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3dfbc-138">OUTPUTS</span></span>

### <span data-ttu-id="3dfbc-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3dfbc-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="3dfbc-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3dfbc-140">NOTES</span></span>

## <span data-ttu-id="3dfbc-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3dfbc-141">RELATED LINKS</span></span>

[<span data-ttu-id="3dfbc-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3dfbc-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="3dfbc-143">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3dfbc-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="3dfbc-144">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3dfbc-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="3dfbc-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3dfbc-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="3dfbc-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3dfbc-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="3dfbc-147">Parar-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3dfbc-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="3dfbc-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3dfbc-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
