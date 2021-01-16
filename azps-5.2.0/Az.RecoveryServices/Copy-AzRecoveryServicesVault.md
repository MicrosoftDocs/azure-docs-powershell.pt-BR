---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 68c2914c694dbfb89044597fc35582a83f426b6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259641"
---
# <span data-ttu-id="81ccd-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="81ccd-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="81ccd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="81ccd-103">Copia dados de um cofre em uma região para um cofre em outra região.</span><span class="sxs-lookup"><span data-stu-id="81ccd-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="81ccd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81ccd-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="81ccd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81ccd-105">DESCRIPTION</span></span>
<span data-ttu-id="81ccd-106">O cmdlet **Copy-AzRecoveryServicesVault** copia dados de um cofre em uma região para um cofre em outra região.</span><span class="sxs-lookup"><span data-stu-id="81ccd-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="81ccd-107">Atualmente, só damos suporte à movimentação de dados em nível de cofre.</span><span class="sxs-lookup"><span data-stu-id="81ccd-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="81ccd-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81ccd-108">EXAMPLES</span></span>

### <span data-ttu-id="81ccd-109">Exemplo 1: copiar dados do vault1 para o vault2</span><span class="sxs-lookup"><span data-stu-id="81ccd-109">Example 1: Copy data from vault1 to vault2</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

<span data-ttu-id="81ccd-110">Os dois primeiros cmdlets buscam o cofre de serviços de recuperação vault1 e vault2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="81ccd-110">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="81ccd-111">O segundo comando dispara uma movimentação de dados completa de vault1 para vault2.</span><span class="sxs-lookup"><span data-stu-id="81ccd-111">The second command triggers a complete data move from vault1 to vault2.</span></span> 

### <span data-ttu-id="81ccd-112">Exemplo 2: copiar dados do vault1 para o vault2 apenas com itens com falha</span><span class="sxs-lookup"><span data-stu-id="81ccd-112">Example 2: Copy data from vault1 to vault2 with only failed items</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
``` 

<span data-ttu-id="81ccd-113">Os dois primeiros cmdlets buscam o cofre de serviços de recuperação vault1 e vault2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="81ccd-113">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="81ccd-114">O segundo comando dispara uma movimentação de dados parciais de vault1 para vault2 apenas com os itens que falhavam nas operações de movimentação anteriores.</span><span class="sxs-lookup"><span data-stu-id="81ccd-114">The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.</span></span>

## <span data-ttu-id="81ccd-115">OS</span><span class="sxs-lookup"><span data-stu-id="81ccd-115">PARAMETERS</span></span>

### <span data-ttu-id="81ccd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81ccd-116">-DefaultProfile</span></span>
<span data-ttu-id="81ccd-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81ccd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ccd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="81ccd-118">-Force</span></span>
<span data-ttu-id="81ccd-119">Força a operação de movimentação de dados (impede a caixa de diálogo de confirmação) sem solicitar confirmação para o tipo de redundância do armazenamento do cofre de destino.</span><span class="sxs-lookup"><span data-stu-id="81ccd-119">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="81ccd-120">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="81ccd-120">This parameter is optional.</span></span> 

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

### <span data-ttu-id="81ccd-121">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="81ccd-121">-RetryOnlyFailed</span></span>
<span data-ttu-id="81ccd-122">Parâmetro de alternância para testar a movimentação de dados somente para contêineres no cofre de origem que ainda não foram movidos.</span><span class="sxs-lookup"><span data-stu-id="81ccd-122">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="81ccd-123">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="81ccd-123">-SourceVault</span></span>
<span data-ttu-id="81ccd-124">O objeto do cofre de origem a ser movido.</span><span class="sxs-lookup"><span data-stu-id="81ccd-124">The source vault object to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81ccd-125">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="81ccd-125">-TargetVault</span></span>
<span data-ttu-id="81ccd-126">O objeto do cofre de destino em que os dados têm que ser movidos.</span><span class="sxs-lookup"><span data-stu-id="81ccd-126">The target vault object where the data has to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81ccd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81ccd-127">CommonParameters</span></span>
<span data-ttu-id="81ccd-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81ccd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81ccd-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81ccd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81ccd-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81ccd-130">INPUTS</span></span>

### <span data-ttu-id="81ccd-131">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="81ccd-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="81ccd-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81ccd-132">OUTPUTS</span></span>

### <span data-ttu-id="81ccd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="81ccd-133">System.String</span></span>

## <span data-ttu-id="81ccd-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81ccd-134">NOTES</span></span>

## <span data-ttu-id="81ccd-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81ccd-135">RELATED LINKS</span></span>
