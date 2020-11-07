---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
ms.openlocfilehash: cd3e3e2ad33cb01935a2594571145f0667c9a3e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772991"
---
# <span data-ttu-id="8cbde-101">Get-AzRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="8cbde-101">Get-AzRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="8cbde-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8cbde-102">SYNOPSIS</span></span>
<span data-ttu-id="8cbde-103">Verifica se o recurso ARM está em backup ou não.</span><span class="sxs-lookup"><span data-stu-id="8cbde-103">Checks whether your ARM resource is backed up or not.</span></span>

## <span data-ttu-id="8cbde-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8cbde-104">SYNTAX</span></span>

### <span data-ttu-id="8cbde-105">Nome (padrão)</span><span class="sxs-lookup"><span data-stu-id="8cbde-105">Name (Default)</span></span>
```
Get-AzRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cbde-106">IdWorkload</span><span class="sxs-lookup"><span data-stu-id="8cbde-106">IdWorkload</span></span>
```
Get-AzRecoveryServicesBackupStatus -Type <String> -ResourceId <String> -ProtectableObjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cbde-107">%</span><span class="sxs-lookup"><span data-stu-id="8cbde-107">Id</span></span>
```
Get-AzRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8cbde-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8cbde-108">DESCRIPTION</span></span>
<span data-ttu-id="8cbde-109">O comando retornará NULL/Empty se o recurso especificado não estiver protegido em nenhum cofre de serviços de recuperação na assinatura.</span><span class="sxs-lookup"><span data-stu-id="8cbde-109">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="8cbde-110">Se estiver protegido, os detalhes relevantes do cofre serão retornados.</span><span class="sxs-lookup"><span data-stu-id="8cbde-110">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="8cbde-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8cbde-111">EXAMPLES</span></span>

### <span data-ttu-id="8cbde-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8cbde-112">Example 1</span></span>
```
PS C:\> $status = Get-AzRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="8cbde-113">OS</span><span class="sxs-lookup"><span data-stu-id="8cbde-113">PARAMETERS</span></span>

### <span data-ttu-id="8cbde-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cbde-114">-DefaultProfile</span></span>
<span data-ttu-id="8cbde-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8cbde-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cbde-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="8cbde-116">-Name</span></span>
<span data-ttu-id="8cbde-117">Nome do recurso do Azure cujo item representativo precisa ser verificado se já está protegido por algum cofre de serviços de recuperação na assinatura.</span><span class="sxs-lookup"><span data-stu-id="8cbde-117">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

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

### <span data-ttu-id="8cbde-118">-ProtectableObjectName</span><span class="sxs-lookup"><span data-stu-id="8cbde-118">-ProtectableObjectName</span></span>
<span data-ttu-id="8cbde-119">Nome do recurso do Azure cujo item representativo precisa ser verificado se já está protegido por algum cofre de serviços de recuperação na assinatura.</span><span class="sxs-lookup"><span data-stu-id="8cbde-119">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: IdWorkload
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cbde-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cbde-120">-ResourceGroupName</span></span>
<span data-ttu-id="8cbde-121">Nome do grupo de recursos do recurso do Azure cujo item representativo precisa ser verificado se já está protegido por algum cofre Recoveryservices na assinatura.</span><span class="sxs-lookup"><span data-stu-id="8cbde-121">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="8cbde-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cbde-122">-ResourceId</span></span>
<span data-ttu-id="8cbde-123">ID do recurso do Azure cujo item representativo precisa ser verificado se já está protegido por algum cofre Recoveryservices na assinatura.</span><span class="sxs-lookup"><span data-stu-id="8cbde-123">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: IdWorkload, Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cbde-124">-Digite</span><span class="sxs-lookup"><span data-stu-id="8cbde-124">-Type</span></span>
<span data-ttu-id="8cbde-125">Nome do recurso do Azure cujo item representativo precisa ser verificado se já está protegido por algum cofre de serviços de recuperação na assinatura.</span><span class="sxs-lookup"><span data-stu-id="8cbde-125">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, IdWorkload
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cbde-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cbde-126">CommonParameters</span></span>
<span data-ttu-id="8cbde-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cbde-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cbde-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cbde-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cbde-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8cbde-129">INPUTS</span></span>

### <span data-ttu-id="8cbde-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8cbde-130">System.String</span></span>

## <span data-ttu-id="8cbde-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8cbde-131">OUTPUTS</span></span>

### <span data-ttu-id="8cbde-132">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. ResourceBackupStatus</span><span class="sxs-lookup"><span data-stu-id="8cbde-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="8cbde-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8cbde-133">NOTES</span></span>

## <span data-ttu-id="8cbde-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8cbde-134">RELATED LINKS</span></span>
