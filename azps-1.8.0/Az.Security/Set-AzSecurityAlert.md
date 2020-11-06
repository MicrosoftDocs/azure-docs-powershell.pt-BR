---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: c9ed93f1a55f7c8cc52bef68d306f7d246d595a2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599232"
---
# <span data-ttu-id="4fe65-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="4fe65-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="4fe65-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4fe65-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe65-103">Atualiza um estado de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="4fe65-103">Updates a security alert state.</span></span>

## <span data-ttu-id="4fe65-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4fe65-104">SYNTAX</span></span>

### <span data-ttu-id="4fe65-105">SubscriptionLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="4fe65-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fe65-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="4fe65-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fe65-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="4fe65-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fe65-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="4fe65-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fe65-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4fe65-109">DESCRIPTION</span></span>
<span data-ttu-id="4fe65-110">Define um estado de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="4fe65-110">Sets a security alert state.</span></span>

## <span data-ttu-id="4fe65-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4fe65-111">EXAMPLES</span></span>

### <span data-ttu-id="4fe65-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4fe65-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="4fe65-113">Ignora um alerta de segurança que foi gerado.</span><span class="sxs-lookup"><span data-stu-id="4fe65-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="4fe65-114">OS</span><span class="sxs-lookup"><span data-stu-id="4fe65-114">PARAMETERS</span></span>

### <span data-ttu-id="4fe65-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="4fe65-115">-ActionType</span></span>
<span data-ttu-id="4fe65-116">Tipo de ação.</span><span class="sxs-lookup"><span data-stu-id="4fe65-116">Action Type.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fe65-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fe65-117">-DefaultProfile</span></span>
<span data-ttu-id="4fe65-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4fe65-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fe65-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fe65-119">-InputObject</span></span>
<span data-ttu-id="4fe65-120">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="4fe65-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe65-121">-Local</span><span class="sxs-lookup"><span data-stu-id="4fe65-121">-Location</span></span>
<span data-ttu-id="4fe65-122">Ponto.</span><span class="sxs-lookup"><span data-stu-id="4fe65-122">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fe65-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="4fe65-123">-Name</span></span>
<span data-ttu-id="4fe65-124">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4fe65-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fe65-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fe65-125">-PassThru</span></span>
<span data-ttu-id="4fe65-126">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4fe65-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="4fe65-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fe65-127">-ResourceGroupName</span></span>
<span data-ttu-id="4fe65-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4fe65-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe65-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fe65-129">-ResourceId</span></span>
<span data-ttu-id="4fe65-130">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="4fe65-130">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe65-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4fe65-131">-Confirm</span></span>
<span data-ttu-id="4fe65-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fe65-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fe65-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fe65-133">-WhatIf</span></span>
<span data-ttu-id="4fe65-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4fe65-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4fe65-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4fe65-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fe65-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe65-136">CommonParameters</span></span>
<span data-ttu-id="4fe65-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fe65-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe65-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fe65-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe65-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4fe65-139">INPUTS</span></span>

### <span data-ttu-id="4fe65-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4fe65-140">System.String</span></span>

### <span data-ttu-id="4fe65-141">Microsoft. Azure. Commands. Security. Models. Alerts. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="4fe65-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="4fe65-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4fe65-142">OUTPUTS</span></span>

### <span data-ttu-id="4fe65-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4fe65-143">System.Boolean</span></span>

## <span data-ttu-id="4fe65-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4fe65-144">NOTES</span></span>

## <span data-ttu-id="4fe65-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4fe65-145">RELATED LINKS</span></span>
