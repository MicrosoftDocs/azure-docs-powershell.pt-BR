---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125704"
---
# <span data-ttu-id="27232-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="27232-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="27232-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27232-102">SYNOPSIS</span></span>
<span data-ttu-id="27232-103">Obtém as teclas de acesso para uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="27232-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="27232-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27232-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27232-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="27232-105">DESCRIPTION</span></span>
<span data-ttu-id="27232-106">O cmdlet **Get-AzStorageAccountKey** Obtém as teclas de acesso para uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="27232-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="27232-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27232-107">EXAMPLES</span></span>

### <span data-ttu-id="27232-108">Exemplo 1: obter as teclas de acesso para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="27232-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="27232-109">Este comando obtém as chaves da conta de armazenamento do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="27232-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="27232-110">Exemplo 2: obter uma tecla de acesso específica para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="27232-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### <span data-ttu-id="27232-111">Exemplo 3: lista as teclas de acesso para uma conta de armazenamento, inclua as chaves Kerberos (se o Active Directory estiver habilitado)</span><span class="sxs-lookup"><span data-stu-id="27232-111">Example 3: Lists the access keys for a Storage account, include the Kerberos keys (if active directory enabled)</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

<span data-ttu-id="27232-112">Este comando obtém as chaves da conta de armazenamento do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="27232-112">This command gets the keys for the specified Azure Storage account.</span></span>

## <span data-ttu-id="27232-113">OS</span><span class="sxs-lookup"><span data-stu-id="27232-113">PARAMETERS</span></span>

### <span data-ttu-id="27232-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27232-114">-DefaultProfile</span></span>
<span data-ttu-id="27232-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="27232-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27232-116">-ListKerbKey</span><span class="sxs-lookup"><span data-stu-id="27232-116">-ListKerbKey</span></span>
<span data-ttu-id="27232-117">Lista as chaves Kerberos (se o Active Directory estiver habilitada) para a conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="27232-117">Lists the Kerberos keys (if active directory enabled) for the specified storage account.</span></span>
<span data-ttu-id="27232-118">A chave Kerberos é gerada por conta de armazenamento para autenticação baseada em identidade do Azure files com o serviço de domínio do Azure Active Directory (Azure AD DS) ou o serviço de domínio Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="27232-118">Kerberos key is generated per storage account for Azure Files identity based authentication either with Azure Active Directory Domain Service (Azure AD DS) or Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="27232-119">Ele é usado como a senha da identidade registrada no serviço de domínio que representa a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="27232-119">It is used as the password of the identity registered in the domain service that represents the storage account.</span></span> <span data-ttu-id="27232-120">A chave Kerberos não fornece permissão de acesso para executar quaisquer operações de leitura ou gravação de plano de dados ou controle na conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="27232-120">Kerberos key does not provide access permission to perform any control or data plane read or write operations against the storage account.</span></span>

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

### <span data-ttu-id="27232-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="27232-121">-Name</span></span>
<span data-ttu-id="27232-122">Especifica o nome da conta de armazenamento para a qual esse cmdlet obtém chaves.</span><span class="sxs-lookup"><span data-stu-id="27232-122">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="27232-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27232-123">-ResourceGroupName</span></span>
<span data-ttu-id="27232-124">Especifica o nome do grupo de recursos que contém a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="27232-124">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="27232-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27232-125">CommonParameters</span></span>
<span data-ttu-id="27232-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27232-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27232-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27232-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27232-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="27232-128">INPUTS</span></span>

### <span data-ttu-id="27232-129">System. String</span><span class="sxs-lookup"><span data-stu-id="27232-129">System.String</span></span>

## <span data-ttu-id="27232-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="27232-130">OUTPUTS</span></span>

### <span data-ttu-id="27232-131">Microsoft. Azure. Management. Storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="27232-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="27232-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="27232-132">NOTES</span></span>

## <span data-ttu-id="27232-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27232-133">RELATED LINKS</span></span>

[<span data-ttu-id="27232-134">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="27232-134">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


