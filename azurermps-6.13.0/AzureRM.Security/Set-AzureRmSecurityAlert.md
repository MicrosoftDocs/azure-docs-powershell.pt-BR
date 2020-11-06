---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
ms.openlocfilehash: 81cb94cdcb8efa948160d21da3aca709bb86b6fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429342"
---
# <span data-ttu-id="b7e8c-101">Set-AzureRmSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="b7e8c-101">Set-AzureRmSecurityAlert</span></span>

## <span data-ttu-id="b7e8c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="b7e8c-103">Atualiza um estado de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-103">Updates a security alert state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7e8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7e8c-104">SYNTAX</span></span>

### <span data-ttu-id="b7e8c-105">SubscriptionLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="b7e8c-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7e8c-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="b7e8c-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7e8c-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="b7e8c-107">ResourceId</span></span>
```
Set-AzureRmSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7e8c-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="b7e8c-108">InputObject</span></span>
```
Set-AzureRmSecurityAlert [-ActionType <String>] -InputObject <PSSetAlertInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7e8c-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b7e8c-109">DESCRIPTION</span></span>
<span data-ttu-id="b7e8c-110">Define um estado de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-110">Sets a security alert state.</span></span>

## <span data-ttu-id="b7e8c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7e8c-111">EXAMPLES</span></span>

### <span data-ttu-id="b7e8c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b7e8c-112">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="b7e8c-113">Ignora um alerta de segurança que foi gerado.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="b7e8c-114">OS</span><span class="sxs-lookup"><span data-stu-id="b7e8c-114">PARAMETERS</span></span>

### <span data-ttu-id="b7e8c-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="b7e8c-115">-ActionType</span></span>
<span data-ttu-id="b7e8c-116">Tipo de ação.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-116">Action Type.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7e8c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7e8c-117">-DefaultProfile</span></span>
<span data-ttu-id="b7e8c-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7e8c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7e8c-119">-InputObject</span></span>
<span data-ttu-id="b7e8c-120">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-120">Input Object.</span></span>

```yaml
Type: PSSetAlertInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e8c-121">-Local</span><span class="sxs-lookup"><span data-stu-id="b7e8c-121">-Location</span></span>
<span data-ttu-id="b7e8c-122">Ponto.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-122">Location.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7e8c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7e8c-123">-Name</span></span>
<span data-ttu-id="b7e8c-124">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-124">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7e8c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7e8c-125">-PassThru</span></span>
<span data-ttu-id="b7e8c-126">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="b7e8c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7e8c-127">-ResourceGroupName</span></span>
<span data-ttu-id="b7e8c-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-128">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e8c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7e8c-129">-ResourceId</span></span>
<span data-ttu-id="b7e8c-130">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-130">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e8c-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b7e8c-131">-Confirm</span></span>
<span data-ttu-id="b7e8c-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7e8c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7e8c-133">-WhatIf</span></span>
<span data-ttu-id="b7e8c-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7e8c-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7e8c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e8c-136">CommonParameters</span></span>
<span data-ttu-id="b7e8c-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7e8c-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7e8c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e8c-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b7e8c-139">INPUTS</span></span>

### <span data-ttu-id="b7e8c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b7e8c-140">System.String</span></span>
<span data-ttu-id="b7e8c-141">Microsoft. Azure. Commands. Security. cmdlets. Alerts. PSSetAlertInputObject</span><span class="sxs-lookup"><span data-stu-id="b7e8c-141">Microsoft.Azure.Commands.Security.Cmdlets.Alerts.PSSetAlertInputObject</span></span>

## <span data-ttu-id="b7e8c-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b7e8c-142">OUTPUTS</span></span>

### <span data-ttu-id="b7e8c-143">Microsoft. Azure. Commands. Security. Models. Alerts. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="b7e8c-143">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="b7e8c-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b7e8c-144">NOTES</span></span>

## <span data-ttu-id="b7e8c-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7e8c-145">RELATED LINKS</span></span>
