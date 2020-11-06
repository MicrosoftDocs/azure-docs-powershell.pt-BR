---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupStatus.md
ms.openlocfilehash: 00d7bb2c58abfa466b0c4843eb480b43b08b3d90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609757"
---
# <span data-ttu-id="4063d-101">Get-AzureRmRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="4063d-101">Get-AzureRmRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="4063d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4063d-102">SYNOPSIS</span></span>
<span data-ttu-id="4063d-103">Verifica se o recurso ARM está em backup ou não.</span><span class="sxs-lookup"><span data-stu-id="4063d-103">Checks whether your ARM resource is backed up or not.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4063d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4063d-104">SYNTAX</span></span>

### <span data-ttu-id="4063d-105">Nome (padrão)</span><span class="sxs-lookup"><span data-stu-id="4063d-105">Name (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4063d-106">%</span><span class="sxs-lookup"><span data-stu-id="4063d-106">Id</span></span>
```
Get-AzureRmRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4063d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4063d-107">DESCRIPTION</span></span>
<span data-ttu-id="4063d-108">O comando retornará NULL/Empty se o recurso especificado não estiver protegido em nenhum cofre de serviços de recuperação na assinatura.</span><span class="sxs-lookup"><span data-stu-id="4063d-108">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="4063d-109">Se estiver protegido, os detalhes relevantes do cofre serão retornados.</span><span class="sxs-lookup"><span data-stu-id="4063d-109">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="4063d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4063d-110">EXAMPLES</span></span>

### <span data-ttu-id="4063d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4063d-111">Example 1</span></span>
```
PS C:\> $status = Get-AzureRmRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzureRmRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzureRmRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="4063d-112">OS</span><span class="sxs-lookup"><span data-stu-id="4063d-112">PARAMETERS</span></span>

### <span data-ttu-id="4063d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4063d-113">-DefaultProfile</span></span>
<span data-ttu-id="4063d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4063d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4063d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4063d-115">-Name</span></span>
<span data-ttu-id="4063d-116">Nome do recurso do Azure cujo item representativo precisa ser verificado se já está protegido por algum cofre de serviços de recuperação na assinatura.</span><span class="sxs-lookup"><span data-stu-id="4063d-116">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4063d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4063d-117">-ResourceGroupName</span></span>
<span data-ttu-id="4063d-118">Nome do grupo de recursos do recurso do Azure cujo item representativo precisa ser verificado se já está protegido por algum cofre Recoveryservices na assinatura.</span><span class="sxs-lookup"><span data-stu-id="4063d-118">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4063d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4063d-119">-ResourceId</span></span>
<span data-ttu-id="4063d-120">ID do recurso do Azure cujo item representativo precisa ser verificado se já está protegido por algum cofre Recoveryservices na assinatura.</span><span class="sxs-lookup"><span data-stu-id="4063d-120">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4063d-121">-Digite</span><span class="sxs-lookup"><span data-stu-id="4063d-121">-Type</span></span>
<span data-ttu-id="4063d-122">Nome do recurso do Azure cujo item representativo precisa ser verificado se já está protegido por algum cofre de serviços de recuperação na assinatura.</span><span class="sxs-lookup"><span data-stu-id="4063d-122">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4063d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4063d-123">CommonParameters</span></span>
<span data-ttu-id="4063d-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4063d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4063d-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4063d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4063d-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4063d-126">INPUTS</span></span>

### <span data-ttu-id="4063d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4063d-127">System.String</span></span>

## <span data-ttu-id="4063d-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4063d-128">OUTPUTS</span></span>

### <span data-ttu-id="4063d-129">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. ResourceBackupStatus</span><span class="sxs-lookup"><span data-stu-id="4063d-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="4063d-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4063d-130">NOTES</span></span>

## <span data-ttu-id="4063d-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4063d-131">RELATED LINKS</span></span>
