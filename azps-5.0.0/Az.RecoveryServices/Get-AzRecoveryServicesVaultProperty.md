---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 6602f1005877d4e38546338fd44d8fc51991a7b6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125426"
---
# <span data-ttu-id="17427-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="17427-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="17427-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17427-102">SYNOPSIS</span></span>
<span data-ttu-id="17427-103">Retorna as propriedades de um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="17427-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="17427-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17427-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17427-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="17427-105">DESCRIPTION</span></span>
<span data-ttu-id="17427-106">O cmdlet **Get-AzRecoveryServicesVaultProperty** retorna as propriedades de um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="17427-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="17427-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17427-107">EXAMPLES</span></span>

### <span data-ttu-id="17427-108">Exemplo 1: obter propriedades de um cofre</span><span class="sxs-lookup"><span data-stu-id="17427-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
```

<span data-ttu-id="17427-109">O primeiro comando obtém um objeto de cofre e, em seguida, armazena-o na variável $vault.</span><span class="sxs-lookup"><span data-stu-id="17427-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="17427-110">O segundo comando obtém as propriedades do cofre.</span><span class="sxs-lookup"><span data-stu-id="17427-110">The second command Gets the Vault Properties.</span></span>

## <span data-ttu-id="17427-111">OS</span><span class="sxs-lookup"><span data-stu-id="17427-111">PARAMETERS</span></span>

### <span data-ttu-id="17427-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17427-112">-DefaultProfile</span></span>
<span data-ttu-id="17427-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17427-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17427-114">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="17427-114">-VaultId</span></span>
<span data-ttu-id="17427-115">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="17427-115">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17427-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17427-116">CommonParameters</span></span>
<span data-ttu-id="17427-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17427-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17427-118">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17427-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17427-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="17427-119">INPUTS</span></span>

### <span data-ttu-id="17427-120">System. String</span><span class="sxs-lookup"><span data-stu-id="17427-120">System.String</span></span>

## <span data-ttu-id="17427-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="17427-121">OUTPUTS</span></span>

### <span data-ttu-id="17427-122">Microsoft. Azure. Management. Recoveryservices. backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="17427-122">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="17427-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="17427-123">NOTES</span></span>

## <span data-ttu-id="17427-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17427-124">RELATED LINKS</span></span>

[<span data-ttu-id="17427-125">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="17427-125">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="17427-126">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="17427-126">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
