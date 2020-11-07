---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 630dc1a3a14beec147dec3f7bd2601ed0666ad78
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955328"
---
# <span data-ttu-id="17bae-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="17bae-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="17bae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17bae-102">SYNOPSIS</span></span>
<span data-ttu-id="17bae-103">Copia dados de um cofre em uma região para um cofre em outra região.</span><span class="sxs-lookup"><span data-stu-id="17bae-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="17bae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17bae-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="17bae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="17bae-105">DESCRIPTION</span></span>
<span data-ttu-id="17bae-106">O cmdlet **Copy-AzRecoveryServicesVault** copia dados de um cofre em uma região para um cofre em outra região.</span><span class="sxs-lookup"><span data-stu-id="17bae-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="17bae-107">Atualmente, só damos suporte à movimentação de dados em nível de cofre.</span><span class="sxs-lookup"><span data-stu-id="17bae-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="17bae-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17bae-108">EXAMPLES</span></span>

### <span data-ttu-id="17bae-109">Exemplo 1: copiar dados do vault1 para o vault2</span><span class="sxs-lookup"><span data-stu-id="17bae-109">Example 1: Copy data from vault1 to vault2</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a complete data move from vault1 to vault2. 

### Example 2: Copy data from vault1 to vault2 with only failed items
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.

## PARAMETERS

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

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

### <span data-ttu-id="17bae-110">-Force</span><span class="sxs-lookup"><span data-stu-id="17bae-110">-Force</span></span>
<span data-ttu-id="17bae-111">Força a operação de movimentação de dados (impede a caixa de diálogo de confirmação) sem solicitar confirmação para o tipo de redundância do armazenamento do cofre de destino.</span><span class="sxs-lookup"><span data-stu-id="17bae-111">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="17bae-112">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="17bae-112">This parameter is optional.</span></span> 

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

### <span data-ttu-id="17bae-113">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="17bae-113">-RetryOnlyFailed</span></span>
<span data-ttu-id="17bae-114">Parâmetro de alternância para testar a movimentação de dados somente para contêineres no cofre de origem que ainda não foram movidos.</span><span class="sxs-lookup"><span data-stu-id="17bae-114">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="17bae-115">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="17bae-115">-SourceVault</span></span>
<span data-ttu-id="17bae-116">O objeto do cofre de origem a ser movido.</span><span class="sxs-lookup"><span data-stu-id="17bae-116">The source vault object to be moved.</span></span>

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

### <span data-ttu-id="17bae-117">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="17bae-117">-TargetVault</span></span>
<span data-ttu-id="17bae-118">O objeto do cofre de destino em que os dados têm que ser movidos.</span><span class="sxs-lookup"><span data-stu-id="17bae-118">The target vault object where the data has to be moved.</span></span>

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

### <span data-ttu-id="17bae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17bae-119">CommonParameters</span></span>
<span data-ttu-id="17bae-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17bae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17bae-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17bae-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17bae-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="17bae-122">INPUTS</span></span>

### <span data-ttu-id="17bae-123">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="17bae-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="17bae-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="17bae-124">OUTPUTS</span></span>

### <span data-ttu-id="17bae-125">System. String</span><span class="sxs-lookup"><span data-stu-id="17bae-125">System.String</span></span>

## <span data-ttu-id="17bae-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="17bae-126">NOTES</span></span>

## <span data-ttu-id="17bae-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17bae-127">RELATED LINKS</span></span>
