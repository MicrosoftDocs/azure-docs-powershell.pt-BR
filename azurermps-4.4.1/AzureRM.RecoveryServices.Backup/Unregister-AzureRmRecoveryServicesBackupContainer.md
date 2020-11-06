---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c5ab79ca42096ab93102be1288c772cab1ac01f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609604"
---
# <span data-ttu-id="97380-101">Unregister-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="97380-101">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="97380-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97380-102">SYNOPSIS</span></span>
<span data-ttu-id="97380-103">Cancela o registro de um servidor Windows ou outro contêiner do cofre.</span><span class="sxs-lookup"><span data-stu-id="97380-103">Unregisters a Windows Server or other container from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97380-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97380-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97380-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97380-105">DESCRIPTION</span></span>
<span data-ttu-id="97380-106">O cmdlet **Unregister-AzureRmRecoveryServicesBackupContainer** cancela o registro de um servidor Windows ou outro contêiner de backup do cofre.</span><span class="sxs-lookup"><span data-stu-id="97380-106">The **Unregister-AzureRmRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="97380-107">Esse cmdlet Remove referências a um contêiner do cofre.</span><span class="sxs-lookup"><span data-stu-id="97380-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="97380-108">Antes de cancelar o registro de um contêiner, você deve excluir todos os dados protegidos associados a esse contêiner.</span><span class="sxs-lookup"><span data-stu-id="97380-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="97380-109">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="97380-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="97380-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97380-110">EXAMPLES</span></span>

### <span data-ttu-id="97380-111">Exemplo 1: cancelar o registro de um servidor do Windows a partir do cofre</span><span class="sxs-lookup"><span data-stu-id="97380-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzureRmRecoveryServicesContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="97380-112">O primeiro comando obtém o contêiner do Windows chamado server01.contoso.com que está registrado no cofre e, em seguida, armazena-o na variável $Cont.</span><span class="sxs-lookup"><span data-stu-id="97380-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>

<span data-ttu-id="97380-113">O segundo comando cancela o registro do Windows Server especificado do cofre de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="97380-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="97380-114">OS</span><span class="sxs-lookup"><span data-stu-id="97380-114">PARAMETERS</span></span>

### <span data-ttu-id="97380-115">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="97380-115">-Container</span></span>
<span data-ttu-id="97380-116">Especifica um objeto de contêiner de backup para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="97380-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="97380-117">Para obter um objeto **BackupContainer** , use o cmdlet Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="97380-117">To obtain a **BackupContainer** object, use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97380-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97380-118">-DefaultProfile</span></span>
<span data-ttu-id="97380-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97380-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97380-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97380-120">CommonParameters</span></span>
<span data-ttu-id="97380-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97380-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97380-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97380-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97380-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97380-123">INPUTS</span></span>

## <span data-ttu-id="97380-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97380-124">OUTPUTS</span></span>

## <span data-ttu-id="97380-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97380-125">NOTES</span></span>

## <span data-ttu-id="97380-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97380-126">RELATED LINKS</span></span>

[<span data-ttu-id="97380-127">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="97380-127">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)


