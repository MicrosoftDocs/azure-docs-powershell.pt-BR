---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 04813b04d3d2499de549655edb6398550ce25536
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776080"
---
# <span data-ttu-id="e4bc4-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e4bc4-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="e4bc4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4bc4-102">SYNOPSIS</span></span>

## <span data-ttu-id="e4bc4-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4bc4-103">SYNTAX</span></span>

### <span data-ttu-id="e4bc4-104">Eles</span><span class="sxs-lookup"><span data-stu-id="e4bc4-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4bc4-105">S2</span><span class="sxs-lookup"><span data-stu-id="e4bc4-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4bc4-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4bc4-106">DESCRIPTION</span></span>
<span data-ttu-id="e4bc4-107">O cmdlet **Remove-AzWebAppSlot** remove um slot do aplicativo Web do Azure fornecido com o grupo de recursos e o nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="e4bc4-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="e4bc4-108">Esse cmdlet, por padrão, também remove todos os slots e métricas.</span><span class="sxs-lookup"><span data-stu-id="e4bc4-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="e4bc4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4bc4-109">EXAMPLES</span></span>

### <span data-ttu-id="e4bc4-110">Exemplo 1: remover um slot de aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="e4bc4-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "ContosoSlot"
```

<span data-ttu-id="e4bc4-111">Esse comando Remove o slot nomeado Slot001 associado à ContosoSite do aplicativo Web que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="e4bc4-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e4bc4-112">OS</span><span class="sxs-lookup"><span data-stu-id="e4bc4-112">PARAMETERS</span></span>

### <span data-ttu-id="e4bc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4bc4-113">-DefaultProfile</span></span>
<span data-ttu-id="e4bc4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4bc4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4bc4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e4bc4-115">-Force</span></span>
<span data-ttu-id="e4bc4-116">Opção de remoção forçada</span><span class="sxs-lookup"><span data-stu-id="e4bc4-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="e4bc4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4bc4-117">-Name</span></span>
<span data-ttu-id="e4bc4-118">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="e4bc4-118">WebApp Name</span></span>

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

### <span data-ttu-id="e4bc4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4bc4-119">-ResourceGroupName</span></span>
<span data-ttu-id="e4bc4-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e4bc4-120">Resource Group Name</span></span>

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

### <span data-ttu-id="e4bc4-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="e4bc4-121">-Slot</span></span>
<span data-ttu-id="e4bc4-122">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="e4bc4-122">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4bc4-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e4bc4-123">-WebApp</span></span>
<span data-ttu-id="e4bc4-124">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="e4bc4-124">WebApp Object</span></span>

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

### <span data-ttu-id="e4bc4-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e4bc4-125">-Confirm</span></span>
<span data-ttu-id="e4bc4-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4bc4-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4bc4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4bc4-127">-WhatIf</span></span>
<span data-ttu-id="e4bc4-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4bc4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4bc4-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4bc4-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="e4bc4-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4bc4-130">-AsJob</span></span>
<span data-ttu-id="e4bc4-131">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e4bc4-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4bc4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4bc4-132">CommonParameters</span></span>
<span data-ttu-id="e4bc4-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4bc4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4bc4-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4bc4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4bc4-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4bc4-135">INPUTS</span></span>

### <span data-ttu-id="e4bc4-136">Instalação</span><span class="sxs-lookup"><span data-stu-id="e4bc4-136">Site</span></span>
<span data-ttu-id="e4bc4-137">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="e4bc4-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e4bc4-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4bc4-138">OUTPUTS</span></span>

### <span data-ttu-id="e4bc4-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e4bc4-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="e4bc4-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4bc4-140">NOTES</span></span>

## <span data-ttu-id="e4bc4-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4bc4-141">RELATED LINKS</span></span>

[<span data-ttu-id="e4bc4-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e4bc4-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="e4bc4-143">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e4bc4-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="e4bc4-144">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e4bc4-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="e4bc4-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e4bc4-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="e4bc4-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e4bc4-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="e4bc4-147">Parar-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e4bc4-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="e4bc4-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e4bc4-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)