---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
ms.openlocfilehash: 30a25f5101229076bad1219356edde5780364528
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886028"
---
# <span data-ttu-id="f49be-101">New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f49be-101">New-AzEventHubAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="f49be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f49be-102">SYNOPSIS</span></span>
<span data-ttu-id="f49be-103">Gera um token SAS para a regra de autorização eventhub do Azure de namespace/eventhub.</span><span class="sxs-lookup"><span data-stu-id="f49be-103">Generates a SAS token for Azure eventhub authorization rule of namespace/eventhub.</span></span> 

## <span data-ttu-id="f49be-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f49be-104">SYNTAX</span></span>

```
New-AzEventHubAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f49be-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f49be-105">DESCRIPTION</span></span>
<span data-ttu-id="f49be-106">O cmdlet New-AzEventHubAuthorizationRuleSASToken gera um token SAS (Assinatura de Acesso Compartilhado) para um Azure Eventhub Namesapce ou Azure Eventhub</span><span class="sxs-lookup"><span data-stu-id="f49be-106">The New-AzEventHubAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="f49be-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f49be-107">EXAMPLES</span></span>

### <span data-ttu-id="f49be-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f49be-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="f49be-109">Gere token SAS para a regra de autorixação determinada para Namespace com o tempo de início e expiração..</span><span class="sxs-lookup"><span data-stu-id="f49be-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="f49be-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f49be-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="f49be-111">Gere token SAS para a regra de autorixação determinada para Namespace com tempo de expiração.</span><span class="sxs-lookup"><span data-stu-id="f49be-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="f49be-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f49be-112">PARAMETERS</span></span>

### <span data-ttu-id="f49be-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="f49be-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="f49be-114">ARM ResourceId da Regra de Autorização</span><span class="sxs-lookup"><span data-stu-id="f49be-114">ARM ResourceId of the Authoraization Rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f49be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f49be-115">-DefaultProfile</span></span>
<span data-ttu-id="f49be-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f49be-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f49be-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f49be-117">-ExpiryTime</span></span>
<span data-ttu-id="f49be-118">Tempo de Expiração</span><span class="sxs-lookup"><span data-stu-id="f49be-118">Expiry Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f49be-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="f49be-119">-KeyType</span></span>
<span data-ttu-id="f49be-120">Tipo de chave</span><span class="sxs-lookup"><span data-stu-id="f49be-120">Key Type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f49be-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f49be-121">-StartTime</span></span>
<span data-ttu-id="f49be-122">Hora de Início</span><span class="sxs-lookup"><span data-stu-id="f49be-122">Start Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f49be-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f49be-123">-Confirm</span></span>
<span data-ttu-id="f49be-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f49be-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f49be-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f49be-125">-WhatIf</span></span>
<span data-ttu-id="f49be-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f49be-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f49be-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f49be-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f49be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f49be-128">CommonParameters</span></span>
<span data-ttu-id="f49be-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f49be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f49be-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f49be-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f49be-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f49be-131">INPUTS</span></span>

### <span data-ttu-id="f49be-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f49be-132">System.String</span></span>

### <span data-ttu-id="f49be-133">System.Nullable'1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f49be-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f49be-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f49be-134">OUTPUTS</span></span>

### <span data-ttu-id="f49be-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="f49be-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="f49be-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="f49be-136">NOTES</span></span>

## <span data-ttu-id="f49be-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f49be-137">RELATED LINKS</span></span>
