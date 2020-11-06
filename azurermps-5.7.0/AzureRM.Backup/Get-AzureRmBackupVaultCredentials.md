---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvaultcredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: e6e56b1b9026aa0bba4442edc9652372505983ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609529"
---
# <span data-ttu-id="f3c3b-101">Get-AzureRmBackupVaultCredentials</span><span class="sxs-lookup"><span data-stu-id="f3c3b-101">Get-AzureRmBackupVaultCredentials</span></span>

## <span data-ttu-id="f3c3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c3b-103">Baixa o arquivo de credenciais do cofre para um cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="f3c3b-103">Downloads the vault credentials file for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3c3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3c3b-104">SYNTAX</span></span>

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3c3b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f3c3b-105">DESCRIPTION</span></span>
<span data-ttu-id="f3c3b-106">O cmdlet **Get-AzureRmBackupVaultCredentials** baixa o arquivo de credenciais do cofre para um cofre de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="f3c3b-106">The **Get-AzureRmBackupVaultCredentials** cmdlet downloads the vault credentials file for an Azure Backup vault.</span></span>

<span data-ttu-id="f3c3b-107">O backup usa um arquivo de credenciais do cofre para conectar um servidor ao cofre de backup do Azure e registrá-lo.</span><span class="sxs-lookup"><span data-stu-id="f3c3b-107">Backup uses a vault credential file to connect a server to the Azure Backup vault and register it.</span></span>
<span data-ttu-id="f3c3b-108">Você deve registrar um servidor antes que o backup possa enviar dados de backup para o cofre.</span><span class="sxs-lookup"><span data-stu-id="f3c3b-108">You must register a server before Backup can send backup data to the vault.</span></span>

## <span data-ttu-id="f3c3b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3c3b-109">EXAMPLES</span></span>

## <span data-ttu-id="f3c3b-110">OS</span><span class="sxs-lookup"><span data-stu-id="f3c3b-110">PARAMETERS</span></span>

### <span data-ttu-id="f3c3b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c3b-111">-DefaultProfile</span></span>
<span data-ttu-id="f3c3b-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f3c3b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3c3b-113">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="f3c3b-113">-TargetLocation</span></span>
<span data-ttu-id="f3c3b-114">Especifica o caminho de destino onde esse cmdlet armazena o arquivo de credenciais do cofre.</span><span class="sxs-lookup"><span data-stu-id="f3c3b-114">Specifies the destination path where this cmdlet stores the vault credentials file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3b-115">-Cofre</span><span class="sxs-lookup"><span data-stu-id="f3c3b-115">-Vault</span></span>
<span data-ttu-id="f3c3b-116">Especifica o cofre de backup para o qual esse cmdlet obtém um arquivo de credenciais do cofre.</span><span class="sxs-lookup"><span data-stu-id="f3c3b-116">Specifies the Backup vault for which this cmdlet gets a vault credential file.</span></span>
<span data-ttu-id="f3c3b-117">Para obter um objeto **AzureRmBackupVault** , use o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="f3c3b-117">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c3b-118">CommonParameters</span></span>
<span data-ttu-id="f3c3b-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3c3b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c3b-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3c3b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c3b-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f3c3b-121">INPUTS</span></span>

### <span data-ttu-id="f3c3b-122">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="f3c3b-122">AzureRMBackupVault</span></span>

## <span data-ttu-id="f3c3b-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f3c3b-123">OUTPUTS</span></span>

### <span data-ttu-id="f3c3b-124">String</span><span class="sxs-lookup"><span data-stu-id="f3c3b-124">String</span></span>
<span data-ttu-id="f3c3b-125">Esse cmdlet retorna o nome do arquivo de credenciais do cofre.</span><span class="sxs-lookup"><span data-stu-id="f3c3b-125">This cmdlet returns the name of the vault credential file.</span></span>

## <span data-ttu-id="f3c3b-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f3c3b-126">NOTES</span></span>

## <span data-ttu-id="f3c3b-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3c3b-127">RELATED LINKS</span></span>

[<span data-ttu-id="f3c3b-128">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="f3c3b-128">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


