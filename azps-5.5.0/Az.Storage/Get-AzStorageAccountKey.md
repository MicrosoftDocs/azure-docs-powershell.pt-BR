---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116112"
---
# <span data-ttu-id="d6bbd-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d6bbd-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="d6bbd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6bbd-102">SYNOPSIS</span></span>
<span data-ttu-id="d6bbd-103">Obtém as chaves de acesso de uma conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d6bbd-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="d6bbd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6bbd-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6bbd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6bbd-105">DESCRIPTION</span></span>
<span data-ttu-id="d6bbd-106">O cmdlet **Get-AzStorageAccountKey** obtém as teclas de acesso de uma conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d6bbd-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="d6bbd-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d6bbd-107">EXAMPLES</span></span>

### <span data-ttu-id="d6bbd-108">Exemplo 1: Obter as teclas de acesso de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d6bbd-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="d6bbd-109">Esse comando obtém as chaves da conta de Armazenamento do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="d6bbd-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="d6bbd-110">Exemplo 2: Obter uma chave de acesso específica para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d6bbd-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### <span data-ttu-id="d6bbd-111">Exemplo 3: Lista as teclas de acesso de uma conta de armazenamento, incluindo as teclas Kerberos (se o Active Directory estiver habilitado)</span><span class="sxs-lookup"><span data-stu-id="d6bbd-111">Example 3: Lists the access keys for a Storage account, include the Kerberos keys (if active directory enabled)</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

<span data-ttu-id="d6bbd-112">Esse comando obtém as chaves da conta de Armazenamento do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="d6bbd-112">This command gets the keys for the specified Azure Storage account.</span></span>

## <span data-ttu-id="d6bbd-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6bbd-113">PARAMETERS</span></span>

### <span data-ttu-id="d6bbd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6bbd-114">-DefaultProfile</span></span>
<span data-ttu-id="d6bbd-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6bbd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6bbd-116">-ListKerbKey</span><span class="sxs-lookup"><span data-stu-id="d6bbd-116">-ListKerbKey</span></span>
<span data-ttu-id="d6bbd-117">Lista as teclas Kerberos (se o Active Directory estiver habilitado) para a conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="d6bbd-117">Lists the Kerberos keys (if active directory enabled) for the specified storage account.</span></span>
<span data-ttu-id="d6bbd-118">A chave Kerberos é gerada por conta de armazenamento para autenticação baseada em identidade de Arquivos do Azure com o Azure Active Directory Domain Service (Azure AD DS) ou o AD DS (Active Directory Domain Service).</span><span class="sxs-lookup"><span data-stu-id="d6bbd-118">Kerberos key is generated per storage account for Azure Files identity based authentication either with Azure Active Directory Domain Service (Azure AD DS) or Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="d6bbd-119">Ele é usado como a senha da identidade registrada no serviço de domínio que representa a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d6bbd-119">It is used as the password of the identity registered in the domain service that represents the storage account.</span></span> <span data-ttu-id="d6bbd-120">A tecla Kerberos não fornece permissão de acesso para executar quaisquer operações de leitura ou gravação de plano de dados em relação à conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d6bbd-120">Kerberos key does not provide access permission to perform any control or data plane read or write operations against the storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6bbd-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6bbd-121">-Name</span></span>
<span data-ttu-id="d6bbd-122">Especifica o nome da conta de Armazenamento para a qual este cmdlet obtém chaves.</span><span class="sxs-lookup"><span data-stu-id="d6bbd-122">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6bbd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6bbd-123">-ResourceGroupName</span></span>
<span data-ttu-id="d6bbd-124">Especifica o nome do grupo de recursos que contém a conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d6bbd-124">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6bbd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6bbd-125">CommonParameters</span></span>
<span data-ttu-id="d6bbd-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6bbd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6bbd-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6bbd-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6bbd-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="d6bbd-128">INPUTS</span></span>

### <span data-ttu-id="d6bbd-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d6bbd-129">System.String</span></span>

## <span data-ttu-id="d6bbd-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="d6bbd-130">OUTPUTS</span></span>

### <span data-ttu-id="d6bbd-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d6bbd-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="d6bbd-132">Notas</span><span class="sxs-lookup"><span data-stu-id="d6bbd-132">NOTES</span></span>

## <span data-ttu-id="d6bbd-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6bbd-133">RELATED LINKS</span></span>

[<span data-ttu-id="d6bbd-134">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d6bbd-134">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


