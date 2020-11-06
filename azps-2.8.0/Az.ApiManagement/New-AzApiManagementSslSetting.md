---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: 7c4fb7c2147d7daf3307c2895893198ebe805ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598023"
---
# <span data-ttu-id="f6fa0-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="f6fa0-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="f6fa0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6fa0-102">SYNOPSIS</span></span>
<span data-ttu-id="f6fa0-103">Cria uma instância de PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="f6fa0-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="f6fa0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6fa0-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6fa0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6fa0-105">DESCRIPTION</span></span>
<span data-ttu-id="f6fa0-106">Comando auxiliar para criar uma instância de PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="f6fa0-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="f6fa0-107">Esse comando deve ser usado com o comando New-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f6fa0-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="f6fa0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6fa0-108">EXAMPLES</span></span>

### <span data-ttu-id="f6fa0-109">Exemplo 1: criar uma configuração SSL para habilitar o TLS 1,0 em backend e front-end</span><span class="sxs-lookup"><span data-stu-id="f6fa0-109">Example 1 : Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="f6fa0-110">Crie uma nova instância de PsApiManagementSslSetting para habilitar o TLSv 1,0 em ambos os front-end (entre cliente e APIM) e back-end (entre APIM e back-end) do gateway do ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f6fa0-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="f6fa0-111">OS</span><span class="sxs-lookup"><span data-stu-id="f6fa0-111">PARAMETERS</span></span>

### <span data-ttu-id="f6fa0-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="f6fa0-112">-BackendProtocol</span></span>
<span data-ttu-id="f6fa0-113">Configurações do protocolo de segurança back-end.</span><span class="sxs-lookup"><span data-stu-id="f6fa0-113">Backend Security protocol settings.</span></span> <span data-ttu-id="f6fa0-114">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f6fa0-114">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fa0-115">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="f6fa0-115">-CipherSuite</span></span>
<span data-ttu-id="f6fa0-116">Configurações de pacotes de codificação SSL na ordem especificada.</span><span class="sxs-lookup"><span data-stu-id="f6fa0-116">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="f6fa0-117">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f6fa0-117">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fa0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6fa0-118">-DefaultProfile</span></span>
<span data-ttu-id="f6fa0-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6fa0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6fa0-120">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="f6fa0-120">-FrontendProtocol</span></span>
<span data-ttu-id="f6fa0-121">Configurações de protocolos de segurança de front-end.</span><span class="sxs-lookup"><span data-stu-id="f6fa0-121">Frontend Security protocols settings.</span></span> <span data-ttu-id="f6fa0-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f6fa0-122">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fa0-123">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="f6fa0-123">-ServerProtocol</span></span>
<span data-ttu-id="f6fa0-124">Configurações de protocolo de servidor como Http2.</span><span class="sxs-lookup"><span data-stu-id="f6fa0-124">Server protocol settings like Http2.</span></span> <span data-ttu-id="f6fa0-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f6fa0-125">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fa0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6fa0-126">CommonParameters</span></span>
<span data-ttu-id="f6fa0-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6fa0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6fa0-128">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6fa0-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6fa0-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6fa0-129">INPUTS</span></span>

### <span data-ttu-id="f6fa0-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f6fa0-130">None</span></span>

## <span data-ttu-id="f6fa0-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6fa0-131">OUTPUTS</span></span>

### <span data-ttu-id="f6fa0-132">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="f6fa0-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="f6fa0-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6fa0-133">NOTES</span></span>

## <span data-ttu-id="f6fa0-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6fa0-134">RELATED LINKS</span></span>

[<span data-ttu-id="f6fa0-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f6fa0-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

