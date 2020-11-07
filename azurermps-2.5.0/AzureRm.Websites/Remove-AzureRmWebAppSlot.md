---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 93db0a86caf381b32293089bd68a6efafc20ef02
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786209"
---
# <span data-ttu-id="7a5ec-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7a5ec-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="7a5ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a5ec-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a5ec-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a5ec-103">SYNTAX</span></span>

### <span data-ttu-id="7a5ec-104">Eles</span><span class="sxs-lookup"><span data-stu-id="7a5ec-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a5ec-105">S2</span><span class="sxs-lookup"><span data-stu-id="7a5ec-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a5ec-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a5ec-106">DESCRIPTION</span></span>
<span data-ttu-id="7a5ec-107">O cmdlet **Remove-AzureRmWebAppSlot** remove um slot do aplicativo Web do Azure fornecido com o grupo de recursos e o nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="7a5ec-108">Esse cmdlet, por padrão, também remove todos os slots e métricas.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="7a5ec-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a5ec-109">EXAMPLES</span></span>

### <span data-ttu-id="7a5ec-110">Exemplo 1: remover um slot de aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="7a5ec-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="7a5ec-111">Esse comando Remove o slot nomeado Slot001 associado à ContosoSite do aplicativo Web que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="7a5ec-112">OS</span><span class="sxs-lookup"><span data-stu-id="7a5ec-112">PARAMETERS</span></span>

### <span data-ttu-id="7a5ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a5ec-113">-DefaultProfile</span></span>
<span data-ttu-id="7a5ec-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a5ec-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7a5ec-115">-Force</span></span>
<span data-ttu-id="7a5ec-116">Opção de remoção forçada</span><span class="sxs-lookup"><span data-stu-id="7a5ec-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="7a5ec-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a5ec-117">-Name</span></span>
<span data-ttu-id="7a5ec-118">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="7a5ec-118">WebApp Name</span></span>

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

### <span data-ttu-id="7a5ec-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a5ec-119">-ResourceGroupName</span></span>
<span data-ttu-id="7a5ec-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7a5ec-120">Resource Group Name</span></span>

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

### <span data-ttu-id="7a5ec-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="7a5ec-121">-Slot</span></span>
<span data-ttu-id="7a5ec-122">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="7a5ec-122">WebApp Slot Name</span></span>

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

### <span data-ttu-id="7a5ec-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7a5ec-123">-WebApp</span></span>
<span data-ttu-id="7a5ec-124">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="7a5ec-124">WebApp Object</span></span>

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

### <span data-ttu-id="7a5ec-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7a5ec-125">-Confirm</span></span>
<span data-ttu-id="7a5ec-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a5ec-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a5ec-127">-WhatIf</span></span>
<span data-ttu-id="7a5ec-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a5ec-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-129">The cmdlet is not run.</span></span>

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
### <span data-ttu-id="7a5ec-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a5ec-130">-AsJob</span></span>
<span data-ttu-id="7a5ec-131">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7a5ec-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a5ec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a5ec-132">CommonParameters</span></span>
<span data-ttu-id="7a5ec-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a5ec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a5ec-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a5ec-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a5ec-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a5ec-135">INPUTS</span></span>

### <span data-ttu-id="7a5ec-136">Instalação</span><span class="sxs-lookup"><span data-stu-id="7a5ec-136">Site</span></span>
<span data-ttu-id="7a5ec-137">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="7a5ec-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7a5ec-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a5ec-138">OUTPUTS</span></span>

### <span data-ttu-id="7a5ec-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7a5ec-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="7a5ec-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a5ec-140">NOTES</span></span>

## <span data-ttu-id="7a5ec-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a5ec-141">RELATED LINKS</span></span>

[<span data-ttu-id="7a5ec-142">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7a5ec-142">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="7a5ec-143">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7a5ec-143">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="7a5ec-144">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7a5ec-144">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="7a5ec-145">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7a5ec-145">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="7a5ec-146">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7a5ec-146">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="7a5ec-147">Parar-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7a5ec-147">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="7a5ec-148">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7a5ec-148">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
