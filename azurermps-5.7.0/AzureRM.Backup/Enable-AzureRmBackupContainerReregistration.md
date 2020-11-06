---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 2605B232-10CA-4426-9917-7C9719C15166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupcontainerreregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
ms.openlocfilehash: f64453995418df572480426e7c2c63e497cf000f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432960"
---
# <span data-ttu-id="2dc35-101">Enable-AzureRmBackupContainerReregistration</span><span class="sxs-lookup"><span data-stu-id="2dc35-101">Enable-AzureRmBackupContainerReregistration</span></span>

## <span data-ttu-id="2dc35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2dc35-102">SYNOPSIS</span></span>
<span data-ttu-id="2dc35-103">Registra novamente um servidor para se conectar a um cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="2dc35-103">Reregisters a server to connect to a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dc35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2dc35-104">SYNTAX</span></span>

```
Enable-AzureRmBackupContainerReregistration [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dc35-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2dc35-105">DESCRIPTION</span></span>
<span data-ttu-id="2dc35-106">O cmdlet **Enable-AzureRmBackupContainerReregistration** registra novamente um servidor para se conectar a um cofre de backup do Azure e continuar a cadeia de pontos de recuperação de backup.</span><span class="sxs-lookup"><span data-stu-id="2dc35-106">The **Enable-AzureRmBackupContainerReregistration** cmdlet reregisters a server to connect to an Azure Backup vault and continue the Backup recovery point chain.</span></span>

<span data-ttu-id="2dc35-107">Se você destruir um servidor, todos os pontos de backup na nuvem permanecerão no cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="2dc35-107">If you destroy a server, all its cloud backup points remain in the Backup vault.</span></span>
<span data-ttu-id="2dc35-108">Se você criar um servidor de substituição e atribuí-lo ao mesmo nome de domínio totalmente qualificado, você poderá conectar o servidor de volta ao mesmo cofre.</span><span class="sxs-lookup"><span data-stu-id="2dc35-108">If you create a replacement server and assign it the same fully qualified domain name, you can connect the server back to the same vault.</span></span>
<span data-ttu-id="2dc35-109">Este cmdlet habilita o backup para fazer backups e adicionar novos pontos de backup ao conjunto existente.</span><span class="sxs-lookup"><span data-stu-id="2dc35-109">This cmdlet enables Backup to make backups and add new backup points to the existing set.</span></span>
<span data-ttu-id="2dc35-110">O novo servidor continua na cadeia de backup.</span><span class="sxs-lookup"><span data-stu-id="2dc35-110">The new the server continues in the backup chain.</span></span>

## <span data-ttu-id="2dc35-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2dc35-111">EXAMPLES</span></span>

## <span data-ttu-id="2dc35-112">OS</span><span class="sxs-lookup"><span data-stu-id="2dc35-112">PARAMETERS</span></span>

### <span data-ttu-id="2dc35-113">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="2dc35-113">-Container</span></span>
<span data-ttu-id="2dc35-114">Especifica o contêiner em que este cmdlet se registra novamente.</span><span class="sxs-lookup"><span data-stu-id="2dc35-114">Specifies the container that this cmdlet reregisters.</span></span>
<span data-ttu-id="2dc35-115">Para obter um **AzureRmBackupContainer** , use o cmdlet Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="2dc35-115">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dc35-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dc35-116">-DefaultProfile</span></span>
<span data-ttu-id="2dc35-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2dc35-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2dc35-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dc35-118">CommonParameters</span></span>
<span data-ttu-id="2dc35-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dc35-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dc35-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dc35-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dc35-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2dc35-121">INPUTS</span></span>

### <span data-ttu-id="2dc35-122">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2dc35-122">AzureBackupContainer</span></span>

## <span data-ttu-id="2dc35-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2dc35-123">OUTPUTS</span></span>

### <span data-ttu-id="2dc35-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2dc35-124">None</span></span>

## <span data-ttu-id="2dc35-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2dc35-125">NOTES</span></span>

## <span data-ttu-id="2dc35-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2dc35-126">RELATED LINKS</span></span>

[<span data-ttu-id="2dc35-127">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2dc35-127">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="2dc35-128">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2dc35-128">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


