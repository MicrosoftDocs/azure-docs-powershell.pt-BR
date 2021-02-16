---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: b06501fafbc573e10ac7d5dba3435dbf96342ba0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411850"
---
# <span data-ttu-id="8adad-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8adad-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="8adad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8adad-102">SYNOPSIS</span></span>
<span data-ttu-id="8adad-103">Altera um ponto de recuperação para um item com falha sobre protegido antes de cometer a operação de failover.</span><span class="sxs-lookup"><span data-stu-id="8adad-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="8adad-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8adad-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8adad-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8adad-105">DESCRIPTION</span></span>
<span data-ttu-id="8adad-106">O **Start-AzRecoveryServicesAsrApplyRecoveryPoint** altera o ponto de recuperação de um item com falha em relação a um item protegido antes de comprometer a operação de failover.</span><span class="sxs-lookup"><span data-stu-id="8adad-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="8adad-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8adad-107">EXAMPLES</span></span>

### <span data-ttu-id="8adad-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8adad-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="8adad-109">Começa a aplicar o ponto de recuperação especificado ao item protegido de replicação e retorna o trabalho ASR usado para controlar a operação.</span><span class="sxs-lookup"><span data-stu-id="8adad-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8adad-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8adad-110">PARAMETERS</span></span>

### <span data-ttu-id="8adad-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="8adad-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="8adad-112">Especifica o arquivo de certificado principal se a criptografia de dados está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="8adad-112">Specifies the primary certificate file if data encryption is being used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8adad-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="8adad-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="8adad-114">Especifica o arquivo de certificado secundário se a criptografia de dados está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="8adad-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8adad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8adad-115">-DefaultProfile</span></span>
<span data-ttu-id="8adad-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8adad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8adad-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8adad-117">-RecoveryPoint</span></span>
<span data-ttu-id="8adad-118">Especifica o objeto do ponto de recuperação correspondente ao ponto de recuperação a ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="8adad-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8adad-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8adad-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8adad-120">Especifica o objeto de item protegido de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="8adad-120">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8adad-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8adad-121">-Confirm</span></span>
<span data-ttu-id="8adad-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8adad-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8adad-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8adad-123">-WhatIf</span></span>
<span data-ttu-id="8adad-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8adad-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8adad-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8adad-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8adad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8adad-126">CommonParameters</span></span>
<span data-ttu-id="8adad-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8adad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8adad-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8adad-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8adad-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="8adad-129">INPUTS</span></span>

### <span data-ttu-id="8adad-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8adad-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="8adad-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="8adad-131">OUTPUTS</span></span>

### <span data-ttu-id="8adad-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="8adad-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8adad-133">Notas</span><span class="sxs-lookup"><span data-stu-id="8adad-133">NOTES</span></span>

## <span data-ttu-id="8adad-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8adad-134">RELATED LINKS</span></span>


