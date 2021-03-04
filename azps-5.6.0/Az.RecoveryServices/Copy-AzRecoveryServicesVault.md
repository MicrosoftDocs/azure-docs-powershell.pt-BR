---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 5b4c7153a844bdc10d2ec487e51ef9f07be0c5c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886418"
---
# <span data-ttu-id="465df-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="465df-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="465df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="465df-102">SYNOPSIS</span></span>
<span data-ttu-id="465df-103">Copia dados de um cofre em uma região para um cofre em outra região.</span><span class="sxs-lookup"><span data-stu-id="465df-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="465df-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="465df-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="465df-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="465df-105">DESCRIPTION</span></span>
<span data-ttu-id="465df-106">O cmdlet **Copy-AzRecoveryServicesVault** copia dados de um cofre em uma região para um cofre em outra região.</span><span class="sxs-lookup"><span data-stu-id="465df-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="465df-107">Atualmente, só há suporte para movimentação de dados de nível de cofre.</span><span class="sxs-lookup"><span data-stu-id="465df-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="465df-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="465df-108">EXAMPLES</span></span>

### <span data-ttu-id="465df-109">Exemplo 1: copiar dados do vault1 para o vault2</span><span class="sxs-lookup"><span data-stu-id="465df-109">Example 1: Copy data from vault1 to vault2</span></span>
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

<span data-ttu-id="465df-110">Os dois primeiros cmdlets buscarão o Recovery Services Vault - vault1 e o vault2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="465df-110">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="465df-111">O segundo comando dispara uma movimentação completa de dados do vault1 para o vault2.</span><span class="sxs-lookup"><span data-stu-id="465df-111">The second command triggers a complete data move from vault1 to vault2.</span></span> 

### <span data-ttu-id="465df-112">Exemplo 2: Copiar dados do vault1 para o vault2 com apenas itens com falha</span><span class="sxs-lookup"><span data-stu-id="465df-112">Example 2: Copy data from vault1 to vault2 with only failed items</span></span>
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```

<span data-ttu-id="465df-113">Os dois primeiros cmdlets buscarão o Recovery Services Vault - vault1 e o vault2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="465df-113">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="465df-114">O segundo comando dispara uma movimentação parcial de dados do vault1 para o vault2 com apenas os itens que falharam nas operações de movimentação anteriores.</span><span class="sxs-lookup"><span data-stu-id="465df-114">The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.</span></span>

## <span data-ttu-id="465df-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="465df-115">PARAMETERS</span></span>

### <span data-ttu-id="465df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="465df-116">-DefaultProfile</span></span>
<span data-ttu-id="465df-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="465df-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="465df-118">-Force</span><span class="sxs-lookup"><span data-stu-id="465df-118">-Force</span></span>
<span data-ttu-id="465df-119">Força a operação de movimentação de dados (impede a caixa de diálogo de confirmação) sem pedir confirmação do tipo de redundância de armazenamento do cofre de destino.</span><span class="sxs-lookup"><span data-stu-id="465df-119">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="465df-120">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="465df-120">This parameter is optional.</span></span> 

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

### <span data-ttu-id="465df-121">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="465df-121">-RetryOnlyFailed</span></span>
<span data-ttu-id="465df-122">Parâmetro Switch para tentar a movimentação de dados apenas para contêineres no cofre de origem que ainda não foram movidos.</span><span class="sxs-lookup"><span data-stu-id="465df-122">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="465df-123">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="465df-123">-SourceVault</span></span>
<span data-ttu-id="465df-124">O objeto do cofre de origem a ser movido.</span><span class="sxs-lookup"><span data-stu-id="465df-124">The source vault object to be moved.</span></span>

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

### <span data-ttu-id="465df-125">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="465df-125">-TargetVault</span></span>
<span data-ttu-id="465df-126">O objeto do cofre de destino para o qual os dados devem ser movidos.</span><span class="sxs-lookup"><span data-stu-id="465df-126">The target vault object where the data has to be moved.</span></span>

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

### <span data-ttu-id="465df-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="465df-127">CommonParameters</span></span>
<span data-ttu-id="465df-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="465df-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="465df-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="465df-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="465df-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="465df-130">INPUTS</span></span>

### <span data-ttu-id="465df-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="465df-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="465df-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="465df-132">OUTPUTS</span></span>

### <span data-ttu-id="465df-133">System.String</span><span class="sxs-lookup"><span data-stu-id="465df-133">System.String</span></span>

## <span data-ttu-id="465df-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="465df-134">NOTES</span></span>

## <span data-ttu-id="465df-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="465df-135">RELATED LINKS</span></span>
