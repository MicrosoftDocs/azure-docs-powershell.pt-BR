---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
ms.openlocfilehash: 4db6ceb0f806aeffd4dc69580da891de567e4e83
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93945036"
---
# <span data-ttu-id="bf63d-101">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bf63d-101">Set-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="bf63d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf63d-102">SYNOPSIS</span></span>
<span data-ttu-id="bf63d-103">Modifica uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bf63d-103">Modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="bf63d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf63d-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf63d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf63d-105">DESCRIPTION</span></span>
<span data-ttu-id="bf63d-106">O cmdlet **set-AzDataLakeStoreAccount** modifica uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bf63d-106">The **Set-AzDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="bf63d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf63d-107">EXAMPLES</span></span>

### <span data-ttu-id="bf63d-108">Exemplo 1: adicionar uma marca a uma conta</span><span class="sxs-lookup"><span data-stu-id="bf63d-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="bf63d-109">Esse comando adiciona a marca especificada à conta data Lake Store chamada ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="bf63d-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="bf63d-110">OS</span><span class="sxs-lookup"><span data-stu-id="bf63d-110">PARAMETERS</span></span>

### <span data-ttu-id="bf63d-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="bf63d-111">-AllowAzureIpState</span></span>
<span data-ttu-id="bf63d-112">Opcionalmente, permitir/bloquear IPs de origem do Azure por meio do firewall.</span><span class="sxs-lookup"><span data-stu-id="bf63d-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf63d-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="bf63d-113">-DefaultGroup</span></span>
<span data-ttu-id="bf63d-114">Especifica a ID de um grupo de diretórios do AzureActive.</span><span class="sxs-lookup"><span data-stu-id="bf63d-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="bf63d-115">Este grupo é o grupo padrão para arquivos e pastas que você criar.</span><span class="sxs-lookup"><span data-stu-id="bf63d-115">This group is the default group for files and folders that you create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf63d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf63d-116">-DefaultProfile</span></span>
<span data-ttu-id="bf63d-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bf63d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf63d-118">-Firewallstate</span><span class="sxs-lookup"><span data-stu-id="bf63d-118">-FirewallState</span></span>
<span data-ttu-id="bf63d-119">Opcionalmente, habilite ou desabilite as regras de firewall existentes.</span><span class="sxs-lookup"><span data-stu-id="bf63d-119">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf63d-120">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="bf63d-120">-KeyVersion</span></span>
<span data-ttu-id="bf63d-121">Se o tipo de criptografia for atribuído pelo usuário, o usuário poderá girar a respectiva versão da chave com esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bf63d-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf63d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf63d-122">-Name</span></span>
<span data-ttu-id="bf63d-123">Especifica o nome de uma conta do repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="bf63d-123">Specifies the name of a Data Lake Store account.</span></span>

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

### <span data-ttu-id="bf63d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf63d-124">-ResourceGroupName</span></span>
<span data-ttu-id="bf63d-125">Especifica o nome do grupo de recursos que contém a conta do data Lake Store a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="bf63d-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf63d-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="bf63d-126">-Tag</span></span>
<span data-ttu-id="bf63d-127">Especifica marcas como pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="bf63d-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="bf63d-128">Você pode usar marcas para identificar uma conta do data Lake Store de outros recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf63d-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf63d-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="bf63d-129">-Tier</span></span>
<span data-ttu-id="bf63d-130">A camada de compromisso desejada para esta conta usar.</span><span class="sxs-lookup"><span data-stu-id="bf63d-130">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf63d-131">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="bf63d-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="bf63d-132">Opcionalmente, habilite ou desabilite os provedores de ID confiáveis existentes.</span><span class="sxs-lookup"><span data-stu-id="bf63d-132">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf63d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf63d-133">CommonParameters</span></span>
<span data-ttu-id="bf63d-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf63d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf63d-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf63d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf63d-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf63d-136">INPUTS</span></span>

### <span data-ttu-id="bf63d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="bf63d-137">System.String</span></span>

### <span data-ttu-id="bf63d-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bf63d-138">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bf63d-139">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. TrustedIdProviderState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="bf63d-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="bf63d-140">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. Firewallstate, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="bf63d-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="bf63d-141">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. Tiertype, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="bf63d-141">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="bf63d-142">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="bf63d-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="bf63d-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf63d-143">OUTPUTS</span></span>

### <span data-ttu-id="bf63d-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bf63d-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="bf63d-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf63d-145">NOTES</span></span>

## <span data-ttu-id="bf63d-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf63d-146">RELATED LINKS</span></span>

[<span data-ttu-id="bf63d-147">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bf63d-147">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="bf63d-148">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bf63d-148">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="bf63d-149">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bf63d-149">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="bf63d-150">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bf63d-150">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


