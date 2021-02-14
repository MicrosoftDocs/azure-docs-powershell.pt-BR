---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: e456ae28bec5f5421dad9c58bc5afb58c4d0d250
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117244"
---
# <span data-ttu-id="4d105-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4d105-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="4d105-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d105-102">SYNOPSIS</span></span>
<span data-ttu-id="4d105-103">Copia dados de um cofre em uma região para um cofre em outra região.</span><span class="sxs-lookup"><span data-stu-id="4d105-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="4d105-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d105-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="4d105-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d105-105">DESCRIPTION</span></span>
<span data-ttu-id="4d105-106">O cmdlet **Copy-AzRecoveryServicesVault** copia dados de um cofre em uma região para um cofre em outra região.</span><span class="sxs-lookup"><span data-stu-id="4d105-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="4d105-107">Atualmente, só há suporte para movimentação de dados no nível do cofre.</span><span class="sxs-lookup"><span data-stu-id="4d105-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="4d105-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4d105-108">EXAMPLES</span></span>

### <span data-ttu-id="4d105-109">Exemplo 1: Copiar dados do cofre1 para o cofre2</span><span class="sxs-lookup"><span data-stu-id="4d105-109">Example 1: Copy data from vault1 to vault2</span></span>
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

<span data-ttu-id="4d105-110">Os dois primeiros cmdlets buscarão o Cofre dos Serviços de Recuperação - o cofre1 e o cofre2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4d105-110">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="4d105-111">O segundo comando aciona uma movimentação completa de dados do cofre1 para o cofre2.</span><span class="sxs-lookup"><span data-stu-id="4d105-111">The second command triggers a complete data move from vault1 to vault2.</span></span> 

### <span data-ttu-id="4d105-112">Exemplo 2: Copiar dados do cofre1 para o cofre2 com apenas itens com falha</span><span class="sxs-lookup"><span data-stu-id="4d105-112">Example 2: Copy data from vault1 to vault2 with only failed items</span></span>
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```

<span data-ttu-id="4d105-113">Os dois primeiros cmdlets buscarão o Cofre dos Serviços de Recuperação - o cofre1 e o cofre2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4d105-113">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="4d105-114">O segundo comando aciona uma movimentação parcial de dados do cofre1 para o cofre2 apenas com os itens que falharam nas operações de movimentação anteriores.</span><span class="sxs-lookup"><span data-stu-id="4d105-114">The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.</span></span>

## <span data-ttu-id="4d105-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d105-115">PARAMETERS</span></span>

### <span data-ttu-id="4d105-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d105-116">-DefaultProfile</span></span>
<span data-ttu-id="4d105-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d105-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d105-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="4d105-118">-Force</span></span>
<span data-ttu-id="4d105-119">Força a operação de movimentação de dados (impede a caixa de diálogo de confirmação) sem pedir confirmação do tipo de redundância de armazenamento do cofre de destino.</span><span class="sxs-lookup"><span data-stu-id="4d105-119">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="4d105-120">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="4d105-120">This parameter is optional.</span></span> 

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

### <span data-ttu-id="4d105-121">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="4d105-121">-RetryOnlyFailed</span></span>
<span data-ttu-id="4d105-122">Alternar parâmetro para tentar mover dados apenas para contêineres no cofre de origem que ainda não foram movidos.</span><span class="sxs-lookup"><span data-stu-id="4d105-122">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="4d105-123">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="4d105-123">-SourceVault</span></span>
<span data-ttu-id="4d105-124">O objeto do cofre de origem a ser movido.</span><span class="sxs-lookup"><span data-stu-id="4d105-124">The source vault object to be moved.</span></span>

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

### <span data-ttu-id="4d105-125">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="4d105-125">-TargetVault</span></span>
<span data-ttu-id="4d105-126">O objeto do cofre de destino para onde os dados devem ser movidos.</span><span class="sxs-lookup"><span data-stu-id="4d105-126">The target vault object where the data has to be moved.</span></span>

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

### <span data-ttu-id="4d105-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d105-127">CommonParameters</span></span>
<span data-ttu-id="4d105-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d105-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d105-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d105-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d105-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="4d105-130">INPUTS</span></span>

### <span data-ttu-id="4d105-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="4d105-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="4d105-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="4d105-132">OUTPUTS</span></span>

### <span data-ttu-id="4d105-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4d105-133">System.String</span></span>

## <span data-ttu-id="4d105-134">Notas</span><span class="sxs-lookup"><span data-stu-id="4d105-134">NOTES</span></span>

## <span data-ttu-id="4d105-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d105-135">RELATED LINKS</span></span>
