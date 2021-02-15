---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
ms.openlocfilehash: d314deb2515907b7d2b668d18d165a7fb0691509
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118670"
---
# <span data-ttu-id="125d6-101">New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="125d6-101">New-AzServiceBusAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="125d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="125d6-102">SYNOPSIS</span></span>
<span data-ttu-id="125d6-103">Gera uma regra de autorização do SAS para servicebus do Azure de namespace/queue/topic.</span><span class="sxs-lookup"><span data-stu-id="125d6-103">Generates a SAS tolen for Azure servicebus authorization rule of namespace/queue/topic.</span></span> 

## <span data-ttu-id="125d6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="125d6-104">SYNTAX</span></span>

```
New-AzServiceBusAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="125d6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="125d6-105">DESCRIPTION</span></span>
<span data-ttu-id="125d6-106">O cmdlet New-AzServiceBusAuthorizationRuleSASToken gera um token SAS (Assinatura de Acesso Compartilhado) para um Azure Eventhub Namesapce ou Azure Eventhub</span><span class="sxs-lookup"><span data-stu-id="125d6-106">The New-AzServiceBusAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="125d6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="125d6-107">EXAMPLES</span></span>

### <span data-ttu-id="125d6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="125d6-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="125d6-109">Gere token SAS para a determinada regra de autorização para Namespace com o tempo de início e expiração..</span><span class="sxs-lookup"><span data-stu-id="125d6-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="125d6-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="125d6-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="125d6-111">Gere token SAS para a determinada regra de autorização para Namespace com tempo de expiração.</span><span class="sxs-lookup"><span data-stu-id="125d6-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="125d6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="125d6-112">PARAMETERS</span></span>

### <span data-ttu-id="125d6-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="125d6-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="125d6-114">Arm ResourceId da Regra de Autorização</span><span class="sxs-lookup"><span data-stu-id="125d6-114">ARM ResourceId of the Authoraization Rule</span></span>

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

### <span data-ttu-id="125d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="125d6-115">-DefaultProfile</span></span>
<span data-ttu-id="125d6-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="125d6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="125d6-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="125d6-117">-ExpiryTime</span></span>
<span data-ttu-id="125d6-118">Tempo de Expiração</span><span class="sxs-lookup"><span data-stu-id="125d6-118">Expiry Time</span></span>

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

### <span data-ttu-id="125d6-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="125d6-119">-KeyType</span></span>
<span data-ttu-id="125d6-120">Tipo de Tecla</span><span class="sxs-lookup"><span data-stu-id="125d6-120">Key Type</span></span>

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

### <span data-ttu-id="125d6-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="125d6-121">-StartTime</span></span>
<span data-ttu-id="125d6-122">Hora de Início</span><span class="sxs-lookup"><span data-stu-id="125d6-122">Start Time</span></span>

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

### <span data-ttu-id="125d6-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="125d6-123">-Confirm</span></span>
<span data-ttu-id="125d6-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="125d6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="125d6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="125d6-125">-WhatIf</span></span>
<span data-ttu-id="125d6-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="125d6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="125d6-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="125d6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="125d6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="125d6-128">CommonParameters</span></span>
<span data-ttu-id="125d6-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="125d6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="125d6-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="125d6-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="125d6-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="125d6-131">INPUTS</span></span>

### <span data-ttu-id="125d6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="125d6-132">System.String</span></span>

### <span data-ttu-id="125d6-133">System.Nullable'1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="125d6-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="125d6-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="125d6-134">OUTPUTS</span></span>

### <span data-ttu-id="125d6-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="125d6-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="125d6-136">Notas</span><span class="sxs-lookup"><span data-stu-id="125d6-136">NOTES</span></span>

## <span data-ttu-id="125d6-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="125d6-137">RELATED LINKS</span></span>