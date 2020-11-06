---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/unregister-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: 6ad62049600f1734beabcc1a322086aad1a92348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431650"
---
# <span data-ttu-id="04140-101">Unregister-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="04140-101">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="04140-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04140-102">SYNOPSIS</span></span>
<span data-ttu-id="04140-103">Cancela o registro de um servidor Windows ou outro contêiner do cofre.</span><span class="sxs-lookup"><span data-stu-id="04140-103">Unregisters a Windows Server or other container from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04140-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04140-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupContainer [-Container] <ContainerBase> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04140-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04140-105">DESCRIPTION</span></span>
<span data-ttu-id="04140-106">O cmdlet **Unregister-AzureRmRecoveryServicesBackupContainer** cancela o registro de um servidor Windows ou outro contêiner de backup do cofre.</span><span class="sxs-lookup"><span data-stu-id="04140-106">The **Unregister-AzureRmRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="04140-107">Esse cmdlet Remove referências a um contêiner do cofre.</span><span class="sxs-lookup"><span data-stu-id="04140-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="04140-108">Antes de cancelar o registro de um contêiner, você deve excluir todos os dados protegidos associados a esse contêiner.</span><span class="sxs-lookup"><span data-stu-id="04140-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="04140-109">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="04140-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="04140-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04140-110">EXAMPLES</span></span>

### <span data-ttu-id="04140-111">Exemplo 1: cancelar o registro de um servidor do Windows a partir do cofre</span><span class="sxs-lookup"><span data-stu-id="04140-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzureRmRecoveryServicesContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="04140-112">O primeiro comando obtém o contêiner do Windows chamado server01.contoso.com que está registrado no cofre e, em seguida, armazena-o na variável $Cont.</span><span class="sxs-lookup"><span data-stu-id="04140-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>

<span data-ttu-id="04140-113">O segundo comando cancela o registro do Windows Server especificado do cofre de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="04140-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="04140-114">OS</span><span class="sxs-lookup"><span data-stu-id="04140-114">PARAMETERS</span></span>

### <span data-ttu-id="04140-115">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="04140-115">-Container</span></span>
<span data-ttu-id="04140-116">Especifica um objeto de contêiner de backup para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="04140-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="04140-117">Para obter um objeto **BackupContainer** , use o cmdlet Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="04140-117">To obtain a **BackupContainer** object, use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: ContainerBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04140-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04140-118">-DefaultProfile</span></span>
<span data-ttu-id="04140-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04140-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04140-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04140-120">-PassThru</span></span>
<span data-ttu-id="04140-121">Retorne o contêiner a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="04140-121">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="04140-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="04140-122">-Confirm</span></span>
<span data-ttu-id="04140-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04140-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04140-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04140-124">-WhatIf</span></span>
<span data-ttu-id="04140-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="04140-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04140-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="04140-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04140-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04140-127">CommonParameters</span></span>
<span data-ttu-id="04140-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04140-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04140-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04140-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04140-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04140-130">INPUTS</span></span>

### <span data-ttu-id="04140-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="04140-131">None</span></span>
<span data-ttu-id="04140-132">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="04140-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="04140-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04140-133">OUTPUTS</span></span>

## <span data-ttu-id="04140-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04140-134">NOTES</span></span>

## <span data-ttu-id="04140-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04140-135">RELATED LINKS</span></span>

[<span data-ttu-id="04140-136">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="04140-136">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)


